# Funcions

## Introducció

> Una **funció** és un conjunt d'instruccions que s'agrupen per realitzar una tasca concreta i que es poden reutilitzar fàcilment.

Es defineixen mitjançant la paraula reservada `function`, seguida del nom de la funció.

```javascript
function nomFuncio() {
  // Instruccions
  ...
}
```

* El **nombre d'arguments** que es passa a una funció hauria de ser el mateix que el nombre d'arguments que ha indicat la funció. 
* JavaScript **no mostra cap error** si es passen més o menys arguments dels necessaris. 
* L'**ordre dels arguments és fonamental**, les dades que s'esperen en la funció van directament relacionades amb els arguments especificats en la funció. 
* No és obligatori que coincideixi el **nom dels arguments** que utilitza la funció i el nom 
dels arguments que se li passen.


## Arguments o paràmetres

> Les variables que necessiten les funcions s'anomenen **arguments o paràmetres**.

```javascript
<!DOCTYPE html>
<html>
<body>

  <h2>JavaScript Functions</h2>

  <p>This example calls a function which performs a calculation, and returns the result:</p>
  
  <p id="demo"></p>

<script>
  function myFunction(p1, p2) {
      return p1 * p2;
  }
  
  document.getElementById("demo").innerHTML = myFunction(4, 3);
</script>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_functions)

## Documentació i recursos

* **w3schools: Functions** https://www.w3schools.com/js/js_functions.asp