# Events

## Introducció

> Els **events** o **esdeveniments** són "coses" que passen als elements HTML quan el visitant interacciona amb ells.

JavaScript pot "_**reaccionar**_" a aquests esdeveniments.

**Exemples d'esdeveniments HTML:**

- Una pàgina HTML s'acaba de carregar.
- Es clica un botó.
- Prémer una tecla.
- Un camp d'un formulari canvia de valor.

```markup
<!DOCTYPE html>
<html>
<body>

<p>Click the button to display the date.</p>

<button onclick="displayDate()">The time is?</button>

<script>
function displayDate() {
    document.getElementById("demo").innerHTML = Date();
}
</script>

<p id="demo"></p>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_events1)

**Cada element** o etiqueta HTML té la seva pròpia **llista de possibles esdeveniments** que se li poden assignar.

El **nom de cada esdeveniment** es construeix mitjançant el **prefix on**, seguit del **nom en anglès de l'acció** associada a l'esdeveniment.

### **Exemples d'esdeveniment**

**Esdeveniments del ratolí:**

- **onclick**: l'usuari fa clic a un element HTML
- **onmouseover**: l’usuari mou el ratolí a sobre d’un element HTML
- **onmouseout**: l’usuari treu el ratolí d’un element HTML

**Esdeveniments del teclat:**

- **onkeydown**: L’usuari pressiona una tecla
- **onkeyup**

**Esdeveniments de formulari:**

- **onchange**: s’ha canviat un element HTML
- **onfocus**
- **onblur**

**Esdeveniment de finestra:**

- **onload**: el navegador acaba de carregar una pàgina
- **onresize**

## Documentació i recursos

- **w3schools.com: Events** [https://www.w3schools.com/js/js_events.asp](https://www.w3schools.com/js/js_events.asp)

## 4. Esdeveniments

### Afegir un esdeveniment `click`:

**Exemple:** Mostrar un missatge quan l'usuari fa clic a un botó.

```html
<button id="botó">Fes clic aquí</button>
```

```javascript
let botó = document.getElementById("botó");

botó.addEventListener("click", function () {
  alert("Has fet clic al botó!");
});
```

### Esdeveniment `input`:

**Exemple:** Mostrar el text que escriu l'usuari en temps real.

```html
<input type="text" id="entrada" placeholder="Escriu alguna cosa" />
<p id="resultat"></p>
```

```javascript
let entrada = document.getElementById("entrada");
let resultat = document.getElementById("resultat");

entrada.addEventListener("input", function () {
  resultat.textContent = "Has escrit: " + entrada.value;
});
```

---
