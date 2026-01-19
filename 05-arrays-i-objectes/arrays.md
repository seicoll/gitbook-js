# Arrays

## Què és un array?

> Un array és una llista ordenada de valors (elements).

**Exemple d’un array:**

```javascript
let fruits = ["poma", "plàtan", "taronja"];
console.log(fruits);
// Mostra ["poma", "plàtan", "taronja"]
```

## Accedir als elements

Els elements d’un array es poden accedir pel seu índex (comença en 0).

```javascript
console.log(fruits[0]); // "poma"
console.log(fruits[1]); // "plàtan"
console.log(fruits[2]); // "taronja"
```

## Mètodes comuns dels arrays

**Afegir elements**:

```javascript
fruits.push("maduixa"); // Afegir al final
fruits.unshift("raïm"); // Afegir al principi
console.log(fruits);
```

**Eliminar elements**:

```javascript
fruits.pop(); // Treure del final
fruits.shift(); // Treure del principi
console.log(fruits);
```

**Iterar sobre un array**:

- **Amb `for`:**

  ```javascript
  for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
  }
  ```

- **Amb `forEach`:**

  ```javascript
  fruits.forEach(function (fruit) {
    console.log(fruit);
  });
  ```

## Altres mètodes útils:

**Filtrar elements:**

```javascript
let nombres = [10, 20, 30, 40];
let grans = nombres.filter(function (nombre) {
  return nombre > 20;
});
console.log(grans); // [30, 40]
```

**Transformar elements:**

```javascript
let dobles = nombres.map(function (nombre) {
  return nombre * 2;
});
console.log(dobles); // [20, 40, 60, 80]
```
