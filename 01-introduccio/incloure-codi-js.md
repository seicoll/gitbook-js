# Incloure codi JavaScript

[Teoria completa a w3schools.com](https://www.w3schools.com/js/js_whereto.asp)

Podem **incloure codi Javascript** en una pàgina web de 3 formes diferents:

- En el mateix document
- En un fitxer extern
- En els elements HTML

## **En el mateix document**

El codi **Javascript** es troba tancat entre les etiquetes **`<script>`** en qualsevol part del document.

Es recomana la definició del codi en la capçalera del document **`<head>`**.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Exemple de codi JavaScript en el propi document</title>
    <script>
      alert("Hola mòn!!");
    </script>
  </head>

  <body>
    <p>Benvinguts al mòn Javascript</p>
  </body>
</html>
```

[Demo](https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_head)

**Inconvenients:**

- Una modificació del codi requereix **modificar totes les pàgines** que inclouen el bloc de codi.

## **En els elements HMTL**

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>A Web Page</h1>
    <p id="demo">A Paragraph</p>
    <button type="button" onclick="myFunction()">Try it</button>

    <script>
      function myFunction() {
        document.getElementById("demo").innerHTML = "Paragraph changed.";
      }
    </script>
  </body>
</html>
```

[Demo](https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_body)

**Inconvenients:**

- Embruta innecessàriament el codi HTML de la pàgina i **dificulta molt el manteniment** del codi Javascript.

## **En un fitxer extern**

{% code title="index.html" %}

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Exemple de codi JavaScript en un document extern</title>
    <script src="/js/myScript.js"></script>
  </head>
  <body>
    <h2>External JavaScript</h2>

    <p id="demo">A Paragraph.</p>

    <button type="button" onclick="myFunction()">Try it</button>

    <p>(myFunction is stored in an external file called "myScript.js")</p>
  </body>
</html>
```

{% endcode %}

{% code title="myScript.js" %}

```javascript
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

{% endcode %}

[Demo](https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_external)

- Cada etiqueta **`<script>`** només pot enllaçar un únic arxiu.
- En una mateixa pàgina es poden incloure tantes etiquetes _`<script>`_ com siguin necessàries.
- Els arxius de tipus JavaScript són documents de text amb extensió **.js**.&#x20;

---

#### Avantatges <a href="#avantatges" id="avantatges"></a>

- Separa HTML i del codi Javascript.
- Fa que l’HTML i el JavaScript siguin més fàcil de llegir i mantenir
- Qualsevol modificació que es realitza en l'arxiu Javascript es veu reflectida immediatament en totes les pàgines enllaçades.

## Exercicis

### Exercici 1: Creació d'un arxiu HTML + JavaScript:

1. Crea una carpeta al teu ordinador per al projecte (exemple: `curs-javascript`).
2. A VS Code, obre aquesta carpeta (`File > Open Folder`).
3. Afegeix un nou fitxer `index.html` amb el següent contingut bàsic:

   ```html
   <!DOCTYPE html>
   <html lang="ca">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Primera prova amb JavaScript</title>
     </head>
     <body>
       <h1>Hola, món!</h1>
       <script src="script.js"></script>
     </body>
   </html>
   ```

4. Crea un altre fitxer anomenat `script.js` i afegeix-hi el següent codi:
   ```javascript
   console.log("El JavaScript funciona!");
   ```

#### Com executar el codi:

1. Obre el fitxer `index.html` en el navegador (fes doble clic sobre ell).
2. Obre DevTools i vés a la **Consola** per veure el missatge de "El JavaScript funciona!".

---
