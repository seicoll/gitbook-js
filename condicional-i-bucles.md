# Condicionals i bucles

## Switch

```html
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Switch</h2>

<p id="demo"></p>

<script>
var text;
switch (new Date().getDay()) {
    case 6:
        text = "Today is Saturday";
        break;
    case 0:
        text = "Today is Sunday";
        break;
    default:
        text = "Looking forward to the Weekend";
}
document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

[Exemple](https://www.w3schools.com/js/tryit.asp?filename=tryjs_switch)

* Més informació a w3schools.com -Switch: https://www.w3schools.com/js/js_switch.asp
