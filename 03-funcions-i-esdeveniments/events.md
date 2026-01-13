# Esdeveniments (Events)

## Introducció

> Els **events** o **esdeveniments** són "coses" que passen als elements HTML quan el visitant interacciona amb la pàgina web.

JavaScript pot "_**reaccionar**_" a aquests esdeveniments.

**Exemples d'esdeveniments HTML:**

- Una pàgina HTML s'acaba de carregar.
- Es clica un botó.
- Prémer una tecla.
- Un camp d'un formulari canvia de valor.

### Esdeveniment `click`

- **Exemple**: Mostrar la data i hora actual quan l'usuari fa clic a un botó.

  ```html
  <p>Click the button to display the date.</p>

  <button id="boto">The time is?</button>

  <p id="demo"></p>
  ```

  ```js
  // Obtenim el botó pel seu ID
  let boto = document.getElementById("boto");

  // Assignem l'esdeveniment click al botó
  boto.addEventListener("click", displayDate);

  // Funció que mostra la data actual
  function displayDate() {
    document.getElementById("demo").innerHTML = Date();
  }
  ```

  [Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_events1)

### Esdeveniment `input`

- **Exemple**: Mostrar el text que escriu l'usuari en temps real.

  ```html
  <input type="text" id="entrada" placeholder="Escriu alguna cosa" />
  <p id="resultat"></p>
  ```

  ```js
  // Obtenim els elements pel seu ID
  let entrada = document.getElementById("entrada");
  let resultat = document.getElementById("resultat");

  // Assignem l'esdeveniment input al camp de text
  entrada.addEventListener("input", function () {
    resultat.textContent = "Has escrit: " + entrada.value;
  });

  // Hem utilitzat una funció anònima com a manejador de l'esdeveniment
  ```

## Com funcionen els esdeveniments

- Cada element o etiqueta HTML té la seva pròpia **llista de possibles esdeveniments** que se li poden assignar.

### Exemples d'esdeveniment

**Esdeveniments del ratolí:**

- **click**: l'usuari fa clic a un element HTML
- **mouseover**: l’usuari mou el ratolí a sobre d’un element HTML
- **mouseout**: l’usuari treu el ratolí d’un element HTML

**Esdeveniments del teclat:**

- **keydown**: L’usuari pressiona una tecla
- **keyup**

**Esdeveniments de formulari:**

- **change**: s’ha canviat un element HTML
- **focus**
- **blur**

**Esdeveniment de finestra:**

- **load**: el navegador acaba de carregar una pàgina
- **resize**
