# Condicionals i bucles

## Condicionals

## `if`, `else if`, `else`

- Sintaxi bàsica:
  ```
  if (condició) {
      // Codi si la condició és certa
  } else if (altraCondició) {
      // Codi si l'altra condició és certa
  } else {
      // Codi si cap condició és certa
  }
  ```
- Exemple:

  ```javascript
  <!DOCTYPE html>
  <html>
  <body>

  <h2>JavaScript if .. else</h2>

  <p>A time-based greeting:</p>

  <p id="demo"></p>

  <script>
  const time = new Date().getHours();
  let greeting;
  if (time < 10) {
    greeting = "Good morning";
  } else if (time < 20) {
    greeting = "Good day";
  } else {
    greeting = "Good evening";
  }
  document.getElementById("demo").innerHTML = greeting;
  </script>

  </body>
  </html>
  ```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_elseif)

**Més informació a:** [w3schools.com - If](https://www.w3schools.com/js/js_if_else.asp)

## `switch`

```javascript
<!DOCTYPE html>
<html>
<body>
<h1>JavaScript Control Flow</h1>
<h2>The switch Statement</h2>

<p id="demo"></p>

<script>
let day;
let date = new Date().getDay();

switch (date) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
}

document.getElementById("demo").innerHTML = "Today is " + day;
</script>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_switch)

**Més informació a:** [w3schools.com - Switch](https://www.w3schools.com/js/js_switch.asp)

## Bucles

### `for`

```javascript
<!DOCTYPE html>
<html>
<body>
  <h2>JavaScript For Loop</h2>

  <p id="demo"></p>

<script>
  var text = "";
  var i;
  for (i = 0; i < 5; i++) {
      text += "The number is " + i + "<br>";
  }
  document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_loop_for_ex)

**Més informació a:** [w3schools.com - For Loop](https://www.w3schools.com/js/js_loop_for.asp)

### `while`

```javascript
<!DOCTYPE html>
<html>
<body>
  <h2>JavaScript While Loop</h2>

  <p id="demo"></p>

<script>
  var text = "";
  var i = 0;
  while (i < 10) {
    text += "<br>The number is " + i;
    i++;
  }
  document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_while)

**Més informació a:** [w3schools.com - While Loop](https://www.w3schools.com/js/js_loop_while.asp)
