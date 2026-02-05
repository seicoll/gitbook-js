# Axios

## Introducció

> **Axios** és una llibreria de JavaScript basada en _promeses_ que permet realitzar peticions HTTP de manera senzilla tant al navegador (frontend) com a Node.js (backend).

## Instal·lació

Per utilitzar Axios en projectes moderns (React, Node, Vite, Webpack), el més habitual és instal·lar-lo amb **npm**:

```bash
npm install axios
```

I després importar-lo:

```javascript
import axios from "axios";
```

Això elimina la necessitat d'incloure `<script>` al HTML.

```html
<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
```

## Configuració bàsica

### Crear una instància Axios

És recomanable crear una instància per afegir configuració global (baseURL, timeout, headers...):

```javascript
import axios from "axios";

const api = axios.create({
  baseURL: "https://api.example.com",
  timeout: 5000,
});

export default api;
```

Això evita repetir sempre l'URL base i permet afegir interceptors.

### Petició GET

```js
axios
  .get("https://api.example.com/users")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.error(error);
  });
```

```js
api
  .get("/users")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.error(error);
  });
```

### Amb async/await

```js
async function getUsers() {
  try {
    const res = await api.get("/users");
    console.log(res.data);
  } catch (err) {
    console.error(err);
  }
}
```

## Petició POST

```js
axios
  .post("https://api.example.com/users", {
    name: "Joan",
    age: 30,
  })
  .then((r) => console.log(r.data))
  .catch((e) => console.error(e));
```

## Interceptors

```js
axios.interceptors.request.use((config) => {
  config.headers.Authorization = "Bearer TOKEN123";
  return config;
});
```

```javascript
api.interceptors.request.use(
  (config) => {
    const token = localStorage.getItem("token");
    if (token) {
      config.headers.Authorization = `Bearer ${token}`;
    }
    return config;
  },
  (error) => {
    return Promise.reject(error);
  },
);
```

## Gestió d'errors avançada

Axios proporciona `error.response`, `error.request` i `error.message`.

```javascript
api.get("/users").catch((err) => {
  if (err.response) {
    console.log("Error del servidor:", err.response.status, err.response.data);
  } else if (err.request) {
    console.log("Sense resposta del servidor");
  } else {
    console.log("Error en configurar la petició:", err.message);
  }
});
```

## Refresh Tokens (Interceptor de respostes)

Aquest és un dels usos més avançats d'Axios en aplicacions reals.

### Escenari habitual

- El token caduca - el servidor retorna **401 Unauthorized**
- Axios detecta l'error
- Crida el _refresh token endpoint_
- Desa el nou token
- Repeteix automàticament la petició original

### Exemple

```javascript
import axios from "axios";

let isRefreshing = false;
let failedQueue = [];

const processQueue = (error, token = null) => {
  failedQueue.forEach((prom) => {
    if (error) {
      prom.reject(error);
    } else {
      prom.resolve(token);
    }
  });

  failedQueue = [];
};

const api = axios.create({
  baseURL: "https://api.example.com",
});

api.interceptors.response.use(
  (response) => response,
  async (error) => {
    const originalRequest = error.config;

    if (error.response?.status === 401 && !originalRequest._retry) {
      if (isRefreshing) {
        return new Promise((resolve, reject) => {
          failedQueue.push({ resolve, reject });
        }).then((token) => {
          originalRequest.headers.Authorization = `Bearer ${token}`;
          return api(originalRequest);
        });
      }

      originalRequest._retry = true;
      isRefreshing = true;

      try {
        const refreshToken = localStorage.getItem("refresh_token");
        const res = await api.post("/auth/refresh", { refreshToken });

        const newToken = res.data.token;
        localStorage.setItem("token", newToken);

        api.defaults.headers.common.Authorization = `Bearer ${newToken}`;
        processQueue(null, newToken);

        return api(originalRequest);
      } catch (err) {
        processQueue(err, null);
        return Promise.reject(err);
      } finally {
        isRefreshing = false;
      }
    }

    return Promise.reject(error);
  },
);

export default api;
```

## Upload de fitxers amb Axios

```javascript
const formData = new FormData();
formData.append("file", fileObject);

api.post("/upload", formData, {
  headers: { "Content-Type": "multipart/form-data" },
});
```

## Download de fitxers

```javascript
api
  .get("/report.pdf", {
    responseType: "blob",
  })
  .then((res) => {
    const url = window.URL.createObjectURL(new Blob([res.data]));
    const link = document.createElement("a");
    link.href = url;
    link.download = "report.pdf";
    link.click();
  });
```

## On utilitzar-lo?

Axios és molt adequat per:

- Aplicacions React, Vue, Angular
- Gestió de tokens i sessions
- Interceptors avançats
- Configuracions globals
- Upload i download de fitxers
- Projectes Node.js i serveis backend

És preferible a `fetch()` quan cal gestionar:

- Tokens
- Errors complexos
- Capçaleres globalitzades
- Interceptors
