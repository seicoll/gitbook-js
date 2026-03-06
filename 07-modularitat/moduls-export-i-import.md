# Mòduls: export i import

Això implica **exportar** parts d'un fitxer per utilitzar en un o més fitxers, i **importar** les parts que necessites on les necessitis.&#x20;

Per aprofitar aquesta funcionalitat, necessites crear un script al teu document HTML amb un **`type`** de **`module`**.&#x20;

**Exemple:**

```javascript
<script type="module" src="filename.js"></script>
```

Un script que utilitzi aquest **`module`** ara podrà utilitzar les característiques **`import`** i **export.**

## Export

{% code title="car.js" %}

```javascript
export default class Car {
  constructor(color) {
    this.color = color;
  }
}
```

{% endcode %}

## Import

**`Import`** et permet escollir quins parts d'un arxiu o mòdul importar.&#x20;

{% code title="main.js" %}

```javascript
import Car from "./car.js";

let cotxe = new Car("vermell");
```

{% endcode %}

El _`./`_, indica a **`import`** que busqui el fitxer **`car.js`** a la mateixa carpeta que el fitxer actual.&#x20;

La ruta relativa del fitxer (**`./`**) i l'extensió del fitxer (**`.js`**) són necessaris.
