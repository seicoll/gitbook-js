# DOM

En aquesta secció aprendrem a interactuar amb el **DOM (Document Object Model)** per manipular elements HTML amb JavaScript. També introduirem els **esdeveniments**, que permeten respondre a accions dels usuaris, com ara clics o escriptura en formularis.

---

## 1. Què és el DOM?

> **El DOM** (Document Object Model) és una representació estructurada d'una pàgina HTML.

- JavaScript pot accedir, modificar i crear elements del DOM.
- El DOM està organitzat en una estructura d'arbre, on cada element HTML és un **node**.

**Exemple d'un DOM bàsic:**

- HTML original:

```html
<html>
  <head>
    <title>My title</title>
  </head>
  <body>
    <a href="https://example.com">My link</a>
    <h1>My header</h1>
  </body>
</html>
```

- Representació del DOM:

![Exemple DOM](./dom.gif)

---

## 2. Seleccionar Elements del DOM

#### Mètodes per seleccionar elements:

**`document.getElementById`**:

> Selecciona un únic element pel seu `id`.

```javascript
let element = document.getElementById("contenidor");
console.log(element); // Mostra el <div> a la consola
```

**`document.querySelector`**:

> Selecciona el primer element que coincideix amb un selector CSS.

```javascript
let paràgraf = document.querySelector("p");
console.log(paràgraf); // Mostra el primer <p> a la consola
```

**`document.querySelectorAll`**:

> Selecciona tots els elements que coincideixen amb un selector CSS.

```javascript
let paràgrafs = document.querySelectorAll("p");
console.log(paràgrafs); // Mostra una NodeList amb tots els <p>
```

---

## 3. Modificar Elements del DOM

### Modificar contingut:

**Exemple:** Canviar el text d'un paràgraf.

```javascript
let paragraf = document.querySelector("p");

paragraf.textContent = "Hola, JavaScript!";
console.log(paragraf.textContent); // Mostra "Hola, JavaScript!"
```

### Modificar atributs:

**Exemple:** Afegir o canviar un atribut `src` d'una imatge.

```javascript
let element = document.querySelector("img");

element.setAttribute("src", "[nouId](http://www.dogs.com/dog.gif)");
console.log(element.src); // Mostra "http://www.dogs.com/dog.gif"
```

### Modificar estils:

**Exemple:** Canviar el color de text d'un element.

```javascript
let paragraf = document.querySelector("p");

paragraf.style.color = "blue";
paragraf.style.fontSize = "20px";
console.log(paragraf.style.color); // Mostra "blue"
```

### Crear elements des de zero:

**Exemple:** Crear un imatge i afegir-la a la pàgina.

```javascript
let img = document.createElement("img");
img.src = "http://www.dogs.com/dog.gif";

document.body.appendChild(img);
```

---

# Exercicis Pràctics

1. **Canvia el contingut d'un paràgraf**:
   Escriu un codi que canviï el text d'un paràgraf quan l'usuari faci clic a un botó:

   ```html
   <p id="text">Aquest text canviarà.</p>
   <button id="canvia">Canvia el text</button>
   ```

   ```javascript
   let botó = document.getElementById("canvia");
   let text = document.getElementById("text");

   botó.addEventListener("click", function () {
     text.textContent = "El text ha canviat!";
   });
   ```

2. **Canvia el color de fons**:
   Escriu un codi que canvii el color de fons de la pàgina a groc quan es fa clic a un botó:

   ```html
   <button id="color">Canvia el color de fons</button>
   ```

   ```javascript
   let botó = document.getElementById("color");

   botó.addEventListener("click", function () {
     document.body.style.backgroundColor = "yellow";
   });
   ```

3. **Escriu i mostra en temps real**:
   Escriu un programa que mostri el text que l'usuari escriu en una entrada:

   ```html
   <input type="text" id="escritura" placeholder="Escriu alguna cosa" />
   <p id="resposta"></p>
   ```

   ```javascript
   let entrada = document.getElementById("escritura");
   let resposta = document.getElementById("resposta");

   entrada.addEventListener("input", function () {
     resposta.textContent = entrada.value;
   });
   ```

---

## Tasca d'autoaprenentatge

1. Crea una pàgina amb tres botons:
   - Un que canviï el color de text d'un paràgraf.
   - Un que amagui o mostri un paràgraf.
   - Un que mostri una alerta amb el text del paràgraf.
