# Variables i constants

## Declaració de variables

{% hint style="info" %}
Una **variable** és un element que s'utilitza per emmagatzemar un valor.&#x20;
{% endhint %}

Les variables en JavaScript es creen mitjançant la paraula reservada **`let`**.

La paraula reservada **`let`** únicament s'ha d'indicar en definir per primera vegada la variable, el que es denomina **declarar una variable**.

```javascript
let numero_1 = 3;
let numero_2 = 1;
let resultat = numero_1 + numero_2;
```

La paraula reservada **`let`** va ser introduïda a **ES6**, una actualització important per JavaScript, per resoldre aquest problema potencial amb la paraula clau var.

{% hint style="info" %}
És recomanable utilitzar en la decalarició de variables **let**
{% endhint %}

## Diferència entre var i let

La paraula reservada **`var`** també s'utilitza per declarar variables en JavaScript, però té algunes diferències importants respecte a **`let`**.

> **És la forma antiga de declarar variables i no es rencomana el seu ús en codi modern.**

**Diferències:**

- **`var`** NO té un àmbit de bloc.
- **`let`** SÍ té un àmbit de bloc.

**`var`**

```javascript
var elMeuNumero = 123;
if (true) {
  var elMeuNumero = 456;
}
console.log(elMeuNumero); // 456
```

**`let`**

```javascript
let elMeuNumero = 123;
if (true) {
  let elMeuNumero = 456;
}
console.log(elMeuNumero); // 123
```

### Problema en sobreescriure variables

Un dels problemes més grans amb la declaració de variables utilitzant la paraula clau **`var`** és que tu pots fàcilment sobreescriure declaracions de variables:

```javascript
var camper = "James";
var camper = "David";
console.log(camper);
```

Al codi anterior, la variable **`camper`** es declara originalment com `James`, i s'anul·la per ser `David`. La consola després mostra la cadena de text `David`.

En una aplicació petita, potser no us trobeu amb aquest tipus de problema. Però a mesura que el teu codi base es fa més gran, **pot ser que accidentalment sobrescriguis una variable que no tenies la intenció de fer**.&#x20;

Com que aquest comportament no causa un error, la cerca i correcció d'errors es torna més difícil.

### No és necessari declarar les variables

Una de les característiques més sorprenents de Javascript per als programadors habituats a altres llenguatges de programació és que **no és necessari declarar variables**.&#x20;

Per tant, es considera correcte:

```javascript
numero_1 = 3;
numero_2 = 1;
resultat = numero_1 + numero_2;
```

Si les variables no estan declarades, JavaScript crea una variable global i assigna el valor corresponent.

{% hint style="danger" %}
Es recomana i serà necessari **declarar totes les variables** que s'hagin d'utilitzar.
{% endhint %}

## Declaració de constants

**Javascript** permet afegir _"variables immutables"_, també conegudes com a **constants**.

L'ús de `const` és una bona pràctica per a variables que no canviaran mai el seu valor, facilita el manteniment de l'aplicació i la llegibilitat.

{% hint style="warning" %}
Les **constants** han de ser declarades i **amb un valor assignat sempre**.
{% endhint %}

**Exemple:**

```javascript
const PI = 3.1416;
PI = 0; // NO permès
```

## Tipus de dades

```javascript
var length = 16; // Number
var length = 16.0; // Number with decimals

var lastName = "Johnson"; // String
var lastName = "Johnson"; // String using single quotes

var condition = true; // Boolean
var cars = ["Saab", "Volvo", "BMW"]; // Array
var x = { firstName: "John", lastName: "Doe" }; // Object
```

### Tipatge en JavaScript

JavaScript és un llenguatge de **tipatge dinàmic** i **debilitat**. Això significa:

1. **Tipatge dinàmic**:

   - Les variables no tenen un tipus fix assignat en el moment de la seva declaració.
   - El tipus d'una variable es pot canviar en temps d'execució.
   - Exemple:

     ```javascript
     let variable = 42; // Inicialment, és un número
     console.log(typeof variable); // "number"

     variable = "Hola!"; // Ara és un text
     console.log(typeof variable); // "string"
     ```

     [Demo](https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_dynamic)

2. **Tipatge debilitat**:
   - JavaScript intenta convertir els valors automàticament quan s'utilitzen diferents tipus junts.
   - Això pot portar a resultats inesperats si no s'és conscient.
   - Exemple:
     ```javascript
     console.log("5" + 5); // "55" (Concatenació perquè "5" és un text)
     console.log("5" - 3); // 2 (Conversió implícita de "5" a número)
     ```

- Exemple d'ús de les varialbles:

  ![](https://lh4.googleusercontent.com/YNgVRrd-Hsg91VoyPXj-0meHOVx1lGmn6lGhkkSVPsXTTzPfC6QFMm5Cl47LNn5d6WBC1KMAZk8fe-TGNIAW98qlEasUlrFD5sonGkpnfx1F_qmOdYFEa4kFhguLiOK77dI9GcJoZQ)
