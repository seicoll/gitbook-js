# Operadors

{% hint style="info" %}
Els **operadors** permeten **manipular el valor de les variables**, realitzar operacions matemàtiques amb els valors i **comparar** les diferents variables.
{% endhint %}

### Assignació

{% hint style="info" %}
L'operador d'**assignació \( `=` \)** serveix per emmagatzemar un valor en una variable.
{% endhint %}

Assigna la part de la dreta de l'igual a la part de l'esquerra. A la dreta es col·loquen els valors finals i a l'esquerra generalment es col·loca una variable on volem guardar la dada.

```javascript
var numero1 = 3; 
var numero2 = 4; 
 
5 = numero1;
/* Error, l'assignació sempre es realitza a una variable, pel que en l'esquerra 
no es pot indicar un nombre */ 
 
numero1 = 5; 			    // Ara, la variable numero1 val 5 

numero1 = numero2;    // Ara, la variable numero1 val 4 
```

### Operadors aritmètics

{% hint style="info" %}
S'utilitzen per a la realització d'**operacions matemàtiques** simples com la suma, resta o multiplicació.
{% endhint %}

Són les següents:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Operador</th>
      <th style="text-align:left">Nom</th>
      <th style="text-align:left">Descripci&#xF3;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">+</td>
      <td style="text-align:left">Suma</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">-</td>
      <td style="text-align:left">Resta</td>
      <td style="text-align:left">Tamb&#xE9; pot utilitzar-se per canviar el signe d&apos;un n&#xFA;mero
        si s&apos;utilitza amb un sol operand (p.ex. -23).</td>
    </tr>
    <tr>
      <td style="text-align:left">*</td>
      <td style="text-align:left">Multiplicaci&#xF3;</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">/</td>
      <td style="text-align:left">Divisi&#xF3;</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">%</td>
      <td style="text-align:left">Residu</td>
      <td style="text-align:left">
        <p></p>
        <p>Residu de la divisi&#xF3; de dos n&#xFA;meros (<code>3%2</code> retorna <code>1</code> ,
          el residu de dividir <code>3</code> entre <code>2</code>).</p>
      </td>
    </tr>
  </tbody>
</table>

### Operadors d'assignació

Els operadors matemàtics també **es poden combinar amb l'operador d'assignació** per abreviar la seva notació.

```javascript
var nombre1 = 5; 
nombre1 += 3;   // nombre1 = nombre1 + 3 = 8 
nombre1 -= 1;   // nombre1 = nombre1 - 1 = 4 
nombre1 *= 2;   // nombre1 = nombre1 * 2 = 10 
nombre1 /= 5;   // nombre1 = nombre1 / 5 = 1 
nombre1 %= 4;   // nombre1 = nombre1 % 4 = 1  
```

### Increment i decrement

{% hint style="info" %}
S'utilitza per **incrementar** \(**`++`**\) o **decrementar** \(**`--`**\) en una unitat el valor d'una variable.
{% endhint %}

Aquests dos operadors només són vàlids per a les variables numèriques.

Dues formes equivalents d’**incrementar un nombre**:

```javascript
var nombre = 5; 
nombre = nombre + 1; 
alerta(nombre); // nombre = 6

/* Equival a... */

var nombre = 5; 
++nombre; 
alerta(nombre); // nombre = 6
```

Dues formes equivalents de **decrementar** un nombre:

```javascript
var nombre = 5; 
nombre = nombre - 1; 
alerta(nombre); // nombre = 4

/* Equival a ... */

var nombre = 5; 
--nombre; 
alerta(nombre); // nombre = 4
```

Els operadors d'increment i decrement no només es poden indicar com a prefix del nom de la variable, sinó que ho poden fer com a **sufix**.

```javascript
var nombre = 5; 
nombre++; 
alerta(nombre); // nombre = 6
```

Si l'operador **`++`** s'indica com a prefix del nom de la variable, el valor s'incrementa **abans** de fer qualsevol altra operació.

```javascript
var nombre1 = 5; 
var nombre2 = 2; 
nombre3 = ++nombre1 + nombre2; // nombre3 = 8
```

Si l'operador **`++`** s'indica com a sufix del nom de la variable, el valor s'incrementa **després** d'executar la sentència en la qual apareix.

```javascript
var nombre1 = 5; 
var nombre2 = 2; 
nombre3 = nombre1++ + nombre2; // nombre3 = 7
```

### Operadors lògics

{% hint style="info" %}
Els **operadors lògics** serveixen per realitzar operacions lògiques, que són aquelles que donen com resultat valor boolèa \(**`true`** o **`false`** \).
{% endhint %}

**Operador AND \(`&&`\)**

El resultat només és `true` si els dos operands són `true`.

```javascript
var valor1 = true; 
var valor2 = false; 
resultat = valor1 && valor2; // resultat = false 
 
valor1 = true; 
valor2 = true; 
resultat = valor1 && valor2; // resultat = true
```

**Operador OR \(`||`\)**

El resultat és `true` si algun dels dos operands és `true`.****

```javascript
var valor1 = true; 
var valor2 = false; 
resultat = valor1 || valor2; // resultat = true
 
valor1 = false; 
valor2 = false; 
resultat = valor1 || valor2; // resultat = false
```

#### Operador NO o negació \(`!`\)

S'utilitza per canviar el valor booleà d'una variable. Si una variable val `true`, la negació de la variable passa a valer `false` i viceversa.

```javascript
var visible = true; 
alerta (!visible); // Mostra "false"
```

### **Operadors r**elacionals

Els operadors condicionals s'utilitzen en les expressions condicionals per prendre decisions.

Operadors condicionals:

| Operador | Significat |
| :--- | :--- |


| == | Comprova si dos valors són iguals |
| :--- | :--- |


| != | Comprova si dos valors són diferents |
| :--- | :--- |


| &gt; | Comprova si el primer valor és major que el segon |
| :--- | :--- |


| &gt;= | Comprova si el primer valor és major o igual que el segon |
| :--- | :--- |


| &lt; | Comprova si el primer valor és menor que el segon |
| :--- | :--- |


| &lt;= | Comprova si el primer valor és menor o igual que el segon |
| :--- | :--- |


### Operadors de cadenes



L'operador**`+`**concatena dues cadenes, enganxa la segona cadena a continuació de la primera.

```javascript
let cadena1 = "hola";
let cadena2 = "mundo";
let cadenaConcatenada = cadena1 + cadena2; //cadena concatenada val "holamundo"
```

{% hint style="warning" %}
 L'operador **+** serveix per a dos usos diferents. Si els seus operands són números els **suma**, però si es tracta de cadenes les **concatena**.
{% endhint %}

Javascript és prou llest per entendre quin tipus d'operació realitzar mitjançant una **comprovació dels tipus** que estan implicats en l'operació.

```javascript
let miNumero = 23;
let miCadena1 = "pep";
let miCadena2  = "456";

let resultado1 = miNumero + miCadena1; //resultado1 val "23pep"
let resultado2 = miNumero + miCadena2; //resultado2 val "23456"
let miCadena2 += miNumero; //miCadena2 ahora val "45623"
```

