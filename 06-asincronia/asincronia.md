# Asíncronia

## 1. Introducció a l’asincronia

### Programació síncrona

* Les instruccions s'executen una després de l'altra.

```javascript
console.log("Primera línia");
console.log("Segona línia");
```

### Programació asíncrona

* Permet que algunes operacions (com consultes a un servidor) es facin en **segon pla** mentre altres instruccions continuen executant-se.
* **Exemple amb `setTimeout`:**

```javascript
console.log("Abans del timeout");

setTimeout(function () {
  console.log("Després de 2 segons");
}, 2000);

console.log("Després del timeout (encara que abans del resultat asíncron)");
```

Sortida:

```
Abans del timeout
Després del timeout (encara que abans del resultat asíncron)
Després de 2 segons
```

## 2. Promises

{% hint style="info" %}
Una **Promise** és un objecte que representa el resultat d'una operació asíncrona.

Pot estar:&#x20;

* pendent (**pending**)&#x20;
* resolta (**fulfilled**)&#x20;
* o rebutjada (**rejected**)
{% endhint %}

#### Crear una Promise

**Exemple:**

```javascript
let promesa = new Promise(function (resolve, reject) {
  let èxit = true;

  if (èxit) {
    resolve("Operació exitosa");
  } else {
    reject("Error en l'operació");
  }
});

promesa
  .then(function (resultat) {
    console.log(resultat); // Si es resol
  })
  .catch(function (error) {
    console.error(error); // Si es rebutja
  });
```

### Exemple pràctic: Simular una operació asíncrona

Exemple amb retard:

```javascript
function esperarTemps(ms) {
  return new Promise(function (resolve) {
    setTimeout(function () {
      resolve("Temps completat!");
    }, ms);
  });
}

esperarTemps(2000).then(function (resultat) {
  console.log(resultat); // Mostra "Temps completat!" després de 2 segons
});
```

## 3. `async` i `await`

> La sintaxi `async`/`await` fa que el codi asíncron sembli síncron, facilitant-ne la lectura i comprensió.

### Exemple bàsic:

*   Convertir una Promise amb `async`/`await`:

    ```javascript
    async function exempleAsync() {
      try {
        let resultat = await esperarTemps(2000); // Espera que la Promise es resolgui
        console.log(resultat); // "Temps completat!"
      } catch (error) {
        console.error(error);
      }
    }

    exempleAsync();
    ```

## 4. Treballant amb APIs i `fetch`

### Introducció a `fetch`

> `fetch` és una funció integrada que permet fer peticions HTTP.

**Exemple per obtenir dades d'una API pública:**

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(function (resposta) {
    return resposta.json(); // Convertir la resposta a JSON
  })
  .then(function (dades) {
    console.log(dades); // Mostra les dades obtingudes
  })
  .catch(function (error) {
    console.error("Error en la petició:", error);
  });
```

### Exemple amb `async`/`await`:

**Exemple més net:**

```javascript
async function obtenirDades() {
  try {
    let resposta = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    let dades = await resposta.json();
    console.log(dades);
  } catch (error) {
    console.error("Error en la petició:", error);
  }
}

obtenirDades();
```
