# Organització d'un projecte amb Vite

### Què és Vite?

- **Vite** és una eina moderna per configurar i organitzar projectes de JavaScript.
- Avantatges:
  - Configuració senzilla.
  - Hot-reloading instantani.
  - Suport per a mòduls ESM (ECMAScript Modules).

### Configuració inicial

1. Instal·la **Node.js** (si no està instal·lat): [https://nodejs.org/](https://nodejs.org/).
2. Crea un projecte amb Vite:
   ```bash
   npm create vite@latest projecte-modular --template vanilla
   cd projecte-modular
   npm install
   npm run dev
   ```

### Organitza la carpeta del projecte

Quan treballis amb **Vite**, és important tenir una estructura clara per organitzar el codi. Una proposta bàsica seria la següent:

```
projecte-modular/
├── index.html            # Arxiu HTML principal
├── src/                  # Carpeta de codi font
│   ├── main.js           # Punt d'entrada del projecte
│   ├── utils/            # Carpeta per a mòduls reutilitzables
│   │   ├── calculs.js    # Funcions de càlcul
│   │   ├── format.js     # Funcions de format
│   └── components/       # Carpeta per a components específics
│       ├── boto.js       # Exemple d'un component de botó
├── package.json          # Informació del projecte i dependències
├── vite.config.js        # Configuració de Vite
├── node_modules/         # Dependències instal·lades per npm
```

## Detalls de l'organització:

1. **`index.html`**:
   - El fitxer HTML principal que carrega el codi JavaScript generat per Vite.

2. **`src/`**:
   - Conté tot el codi font del projecte.
   - Subcarpetes:
     - **`utils/`**: Funcions generals reutilitzables (ex.: càlculs, formats).
     - **`components/`**: Estructures o components específics del projecte.

3. **`package.json`**:
   - Conté informació sobre les dependències i scripts del projecte.

4. **`vite.config.js`**:
   - Fitxer opcional per personalitzar la configuració de Vite si cal.

Aquest tipus d'organització ajuda a mantenir el codi estructurat i fàcil de mantenir en projectes més grans.

### Exemple de codi modular amb Vite

1. Crea un fitxer `src/utils/calculs.js`:

```javascript
export function multiplica(a, b) {
  return a * b;
}

export function divideix(a, b) {
  return b !== 0 ? a / b : "No es pot dividir per zero!";
}
```

2. Crea un fitxer `src/main.js`:

```javascript
import { multiplica, divideix } from "./utils/calculs.js";

console.log(multiplica(6, 7)); // 42
console.log(divideix(10, 2)); // 5
```

3. Executa el projecte:

- Utilitza `npm run dev` i obre el navegador a l'adreça que proporciona Vite.

---

## 4. Bones pràctiques d’organització

1. **Separa el codi per funcionalitats**:

- Guarda cada funció o grup de funcions relacionades en fitxers separats.
- Exemple:
  ```
  src/
  ├── api.js (Gestió de dades d’API)
  ├── calculs.js (Operacions matemàtiques)
  ├── main.js (Punt d’entrada del projecte)
  ```

2. **Utilitza noms descriptius**:

- Els noms de fitxers i funcions haurien de descriure la seva funcionalitat.

3. **Evita globals**:

- Treballa amb imports i exports per evitar variables globals que poden causar conflictes.

4. **Documenta el codi**:

- Afegeix comentaris per explicar la funcionalitat de cada funció o mòdul.

---
