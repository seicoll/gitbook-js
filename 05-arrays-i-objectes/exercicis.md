# Exercicis: Arrays i objectes

# Exercici 1: Gestor de noms amb arrays

Crea una pàgina web que permeti gestionar una llista de noms.

Els noms s’han de guardar en un **array ** i la informació s’ha de mostrar dinàmicament a la pàgina.

**La pàgina tindrà:**

- Un camp de text per introduir un nom
- Un botó **Afegir nom**
- Un botó **Eliminar últim**
- Un botó **Ordenar**
- Un botó **Mostrar total d'elements**
- Una llista on es mostrin els noms
- Un paràgraf informatiu

**El programa ha de:**

- Crear un array buit (per exemple: let noms = [])
- Afegir elements a l’array amb `push()`
- Eliminar l’últim element amb `pop()`
- Ordenar l’array amb `sort()`
- Obtenir el nombre d’elements amb `length`
- Recórrer l’array amb `for` o `forEach()`
- Actualitzar el contingut del DOM cada vegada que l’array canviï

**Extensions opcionals**

- Evitar afegir noms buits
- Evitar noms repetits
- Eliminar un nom concret fent clic sobre ell
- Mostrar els noms en majúscules utilitzant `map()`

---

## HTML inicial

```html
<input type="text" id="nameInput" placeholder="Introdueix un nom" />

<button id="addBtn">Afegir nom</button>
<button id="removeBtn">Eliminar últim</button>
<button id="sortBtn">Ordenar</button>
<button id="countBtn">Mostrar total</button>

<ul id="nameList"></ul>
<p id="info"></p>
```

---

## Exercici 2: Gestor d'alumnes amb objectes i arrays

Crea una pàgina web que permeti gestionar les notes d’una classe.

Cada alumne tindrà:

- Nom
- Nota (0–10)

Les dades s’han de guardar en un **array d’objectes**.

```js
let alumnes = [
  { nom: "Anna", nota: 7 },
  { nom: "Marc", nota: 4 },
];
```

### El programa ha de permetre:

**Afegir alumne**

- Llegeix nom i nota
- Crea un objecte { nom, nota }
- Afegeix-lo a l’array amb `push()`
- Mostra’l a la taula

**Calcular mitjana**

- Calcula la mitjana de totes les notes (utilitza un bucle `forEach()`).
- Mostra-la al paràgraf info

**Mostrar aprovats**

- Mostra només alumnes amb nota ≥ 5 (utilizar la funció `filter()`).

**Netejar llista**

- Buida l’array.
- Esborra la taula.

## HTML inicial

```html
<label for="nameInput">Nom de l'alumne:</label>
<input type="text" id="nameInput" placeholder="Nom de l'alumne" />
<label for="gradeInput">Nota:</label>
<input type="number" id="gradeInput" placeholder="Nota" min="0" max="10" />

<button id="addBtn">Afegir alumne</button>
<button id="avgBtn">Calcular mitjana</button>
<button id="passedBtn">Mostrar aprovats</button>
<button id="clearBtn">Netejar llista</button>

<table border="1">
  <thead>
    <tr>
      <th>Nom</th>
      <th>Nota</th>
      <th>Estat (Aprovat o Suspès)</th>
    </tr>
  </thead>
  <tbody id="tableBody"></tbody>
</table>

<p id="info"></p>
```

---
