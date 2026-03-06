# Modularitat i Organització

## Objectiu

Aquesta sessió introdueix els conceptes de **modularitat** i **organització del codi** en JavaScript. Aprendrem a estructurar el codi utilitzant mòduls (importacions i exportacions) i a organitzar millor els nostres projectes amb un entorn modern com **Vite**.

---

## 1. Què és la modularitat?

- La **modularitat** consisteix a dividir el codi en fitxers o blocs més petits i reutilitzables.
- Beneficis:
  - Facilita el manteniment i la lectura del codi.
  - Permet reutilitzar components en diferents parts del projecte.
  - Millora la col·laboració en equips de treball.

---

## 2. Introducció a mòduls en JavaScript

- JavaScript suporta mòduls nativament a través de les paraules clau **`import`** i **`export`**.

- Per aprofitar aquesta funcionalitat, necessites enllaçar el script al teu document HTML amb un **`type`** de **`module`**.

```javascript
<script type="module" src="app.js"></script>
```

### Exportar i importar mòduls

- **Exportar**:
  - Amb `export` es poden compartir funcions, constants o classes entre fitxers.

  <!-- {% code title="utils.js" %} -->

  ```javascript
  // fitxer utils.js
  export function suma(a, b) {
    return a + b;
  }

  export const PI = 3.14;
  ```

  <!-- {% endcode %} -->

- **Importar**:
  - Amb `import` s'accedeix als elements exportats des d'un altre fitxer.

  <!-- {% code title="principal.js" %} -->

  ```javascript
  // fitxer principal.js
  import { suma, PI } from "./utils.js";

  console.log(suma(5, 3)); // 8
  console.log(PI); // 3.14
  ```

  <!-- {% endcode %} -->

- El _`./`_, indica a **`import`** que busqui el fitxer **`car.js`** a la mateixa carpeta que el fitxer actual.&#x20;

- La ruta relativa del fitxer (**`./`**) i l'extensió del fitxer (**`.js`**) són necessaris.

### Exportació per defecte

- Només un element es pot exportar com a **default** per fitxer.

  <!-- {% code title="salutacions.js" %} -->

  ```javascript
  // fitxer salutacions.js
  export default function hola() {
    console.log("Hola, món!");
  }
  ```

  <!-- {% endcode %} -->

<!-- {% code title="principal.js" %} -->

```javascript
// fitxer principal.js
import hola from "./salutacions.js";

hola(); // "Hola, món!"
```

<!-- {% endcode %} -->

### Exemple pràctic amb diversos mòduls

1. Crea un fitxer `math.js`:

   ```javascript
   export function suma(a, b) {
     return a + b;
   }

   export function resta(a, b) {
     return a - b;
   }
   ```

2. Crea un fitxer `app.js`:

   ```javascript
   import { suma, resta } from "./math.js";

   console.log(suma(10, 5)); // 15
   console.log(resta(10, 5)); // 5
   ```

---

## Exercicis Pràctics

1. **Crea un mòdul matemàtic**:

- Crea un fitxer `math.js` que exporti funcions per sumar, restar, multiplicar i dividir. Importa aquestes funcions en un altre fitxer i utilitza-les.

2. **Organitza un projecte amb Vite**:

- Crea un projecte amb Vite i organitza’l amb:
  - Un mòdul `utils.js` per a funcions utilitàries.
  - Un fitxer `main.js` per executar el codi.

3. **Mòdul amb exportació per defecte**:

- Crea un mòdul que exporti per defecte una funció que retorni una salutació personalitzada (`Hola, [Nom]!`).

## Tasca per fer a casa

1. Crea un projecte amb Vite que tingui dos mòduls:

- Un per gestionar operacions amb cadenes de text (convertir a majúscules, comptar caràcters).
- Un altre per gestionar operacions matemàtiques senzilles.
- Combina les funcionalitats en un fitxer principal.

2. Experimenta amb exportacions per defecte i estàndard en diferents mòduls.
