# Variables i constants

{% hint style="info" %}
Una **variable** és un element que s'utilitza per emmagatzemar un valor. 
{% endhint %}

Les variables en JavaScript es creen mitjançant la paraula reservada **`var`**.

La paraula reservada **`var`** únicament s'ha d'indicar en definir per primera vegada la variable, el que es denomina **declarar una variable**.

```javascript
var numero_1 = 3;
var numero_2 = 1;
var resultat = numero_1 + numero_2;
```

### Declaració de variables

En javascript hi ha dues formes de declarar variables: **`var`** i **`let`**.

**Diferències:**

* **`var`**NO té un àmbit de bloc.
* **`let`**SÍ té un àmbit de bloc.

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

### 

Una de les característiques més sorprenents de Javascript per als programadors habituats a altres llenguatges de programació és que **no és necessari declarar variables**. 

Per tant es considera correcte:

```javascript
numero_1 = 3;
numero_2 = 1;
resultat = numero_1 + numero_2;
```

Si les variables no estan declarades, JavaScript crea una variable global i assigna el valor corresponent.

{% hint style="danger" %}
Es recomana i serà necessari **declarar totes les variables** que s'hagin d'utilitzar.
{% endhint %}

#### Exemple d'ús de variables

![](https://lh4.googleusercontent.com/YNgVRrd-Hsg91VoyPXj-0meHOVx1lGmn6lGhkkSVPsXTTzPfC6QFMm5Cl47LNn5d6WBC1KMAZk8fe-TGNIAW98qlEasUlrFD5sonGkpnfx1F_qmOdYFEa4kFhguLiOK77dI9GcJoZQ)

### Declaració de constants

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



