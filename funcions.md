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