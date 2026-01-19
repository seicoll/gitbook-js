# Arrays

## Què és un array?

> Un **array** és una llista ordenada de valors (elements).

Els elements poden ser de **qualsevol tipus**: nombres, cadenes de text, objectes, altres arrays, etc.

**Exemple d’un array:**

```javascript
// Array buit
const emptyArray = [];

// Array amb elements
const fruits = ["poma", "plàtan", "taronja"];
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
fruits.push("maduixa"); // Afegeix l'element al final
fruits.unshift("raïm"); // Afegeix l'element al principi
console.log(fruits); // ["raïm", "poma", "plàtan", "taronja", "maduixa"]
```

**Eliminar elements**:

```javascript
fruits.pop(); // Treure l'element del final
fruits.shift(); // Treure l'element del principi
console.log(fruits); // ["poma", "plàtan", "taronja"]
```

**Iterar sobre un array**:

- **Amb `for`:**

  ```javascript
  for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]); // Mostra cada fruita
  }

  // Sortida:
  // maduixa
  // kiwi
  // mango
  // taronja
  ```

- **Amb `forEach`:**

  Executa una funció proporcionada una vegada per cada element de l'array.

  ```javascript
  fruits.forEach(function (fruit) {
    console.log(fruit);
  });

  // Sortida:
  // maduixa
  // kiwi
  // mango
  // taronja
  ```

## Altres mètodes útils

**Ordenar elements:**

`sort()` ordenar elements en ordre ascendent:

```javascript
const numbers = [4, 2, 5, 1, 3];
numbers.sort();

console.log(numbers); // [1, 2, 3, 4, 5]
```

`reverse()` invertir l'ordre dels elements:

```javascript
const fruits = ["maduixa", "kiwi", "mango", "taronja"];
fruits.reverse();

console.log(fruits); // ['taronja', 'mango', 'kiwi', 'maduixa']
```

**Filtrar elements:**

Crea un nou array amb els elements que compleixen una determinada condició.

```javascript
let nombres = [10, 20, 30, 40];
let grans = nombres.filter(function (nombre) {
  return nombre > 20;
});
console.log(grans); // [30, 40]
```

**Transformar elements:**

Crea un nou array amb els resultats de l'execució d'una funció en cada element de l'array original.

```javascript
let nombres = [10, 20, 30, 40];
let dobles = nombres.map(function (nombre) {
  return nombre * 2;
});
console.log(dobles); // [20, 40, 60, 80]
```
