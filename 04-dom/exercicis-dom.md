# Exercicis: Manipulació del DOM

## Exercici 1: Manipulació bàsica del DOM

Crea una pàgina amb tres botons:

- Un que canviï el color de text d'un paràgraf.
- Un que amagui o mostri un paràgraf.
- Un que mostri una alerta amb el text del paràgraf.

## Exercici 2: Llista dinàmica de tasques (To-Do)

Implementa una llista de tasques on l'usuari pugui afegir nous elements i eliminar-los.

Crea una pàgina web amb:

- Un camp de text
- Un botó **_Afegir_**
- Una llista (`<ul>`)

Quan l’usuari escrigui una tasca i premi el botó:

- Es crearà un nou element `<li>` amb el text introduït.
- Cada `<li>` tindrà un botó **_Eliminar_**.
- En clicar **_Eliminar_**, la tasca desapareixerà de la llista.

### Fitxer: `index.html`

```html
<!DOCTYPE html>
<html lang="ca">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>La llista de tasques</h1>
    <ul id="todo-list"></ul>
    <label for="item-input">Nova tasca:</label>
    <input type="text" id="item-input" placeholder="Afegeix una tasca" />
    <button id="btn-add">Afegeix</button>
    <script src="app.js"></script>
  </body>
</html>
```

### Explicació dels elements HTML

| Element    | Atribut `id` | Funció                                  |
| ---------- | ------------ | --------------------------------------- |
| `<ul>`     | `todo-list`  | Contenidor on apareixeran les tasques   |
| `<input>`  | `item-input` | Camp de text per escriure noves tasques |
| `<button>` | `add-button` | Botó per afegir una nova tasca          |

> ⚠️ **Important**: El `<script>` es col·loca al final del `<body>` per assegurar que tots els elements HTML ja existeixen quan s'executa el JavaScript.

---

## 2. JavaScript - Pas a Pas

Ara crearem el fitxer `app.js` que contindrà tota la lògica de la nostra aplicació.

### Pas 2.1: Seleccionar els elements del DOM

El primer que hem de fer és obtenir referències als elements HTML que necessitem manipular.

```javascript
// Elements del DOM
const todoList = document.getElementById("todo-list");
const itemInput = document.getElementById("item-input");
const addButton = document.getElementById("btn-add");
```

---

### Pas 2.2: Crear la funció per afegir articles

Ara crearem una funció que s'executarà cada vegada que l'usuari vulgui afegir un article.

```javascript
// Funció per afegir una tasca a la llista
function addItem() {
  // Obtenir el text de l'input
  const itemText = itemInput.value.trim();
  // trim() elimina espais en blanc al principi i al final

  // Comprova que l'usuari ha escrit alguna cosa
  if (itemText === "") {
    alert("Si us plau, escriu una tasca");
    return; // Surt de la funció si no hi ha text
  }

  // Crear el nou element de llista
  const li = document.createElement("li");
  // Assignar el text a l'element
  li.textContent = itemText;
  // Afegeix l'element com a fill de la llista `<ul>`
  todoList.appendChild(li);

  // Netejar el camp d'entrada
  itemInput.value = "";
  // Posar el focus de nou al camp d'entrada
  itemInput.focus();
}
```

---

### Pas 2.3: Afegir els Event Listeners

Finalment, hem de connectar els esdeveniments de l'usuari amb la nostra funció.

```javascript
// Event listeners
addButton.addEventListener("click", addItem);

// Permetre afegir amb la tecla Enter
itemInput.addEventListener("keypress", function (event) {
  if (event.key === "Enter") {
    addItem();
  }
});
```

---

### Pas 2.4: Afegir la funcionalitat d'eliminar tasques

Per últim, afegirem la funcionalitat per eliminar tasques quan es faci clic al botó **_Eliminar_**.

```javascript
// Funció per eliminar una tasca
function removeItem(event) {
  // Obtenir el pare del botó (el <li>)
  const li = event.target.parentElement;

  // Eliminar l'element de la llista
  todoList.removeChild(li);
}

// Modificar la funció addItem per afegir el botó d'eliminar
function addItem() {
  const itemText = itemInput.value.trim();
  if (itemText === "") {
    alert("Si us plau, escriu una tasca");
    return;
  }

  const li = document.createElement("li");
  li.textContent = itemText;

  // Crear el botó d'eliminar
  const deleteButton = document.createElement("button");
  deleteButton.textContent = "Eliminar";

  // Afegir event listener al botó
  deleteButton.addEventListener("click", removeItem);

  // Afegir el botó al <li>
  li.appendChild(deleteButton);

  todoList.appendChild(li);
  itemInput.value = "";
  itemInput.focus();
}
```
