# Exercicis: Asincronia i APIs

## Exercici 1: Crida a una API pública amb `fetch`

Crear una mini-aplicació web (HTML + JS) que consulti la **PokéAPI** amb `fetch` i mostri informació de Pokémon de forma dinàmica.

> API base: `https://pokeapi.co/api/v2/`

### 1. Interfície (HTML)

Crea una pàgina amb:

- Un input de text per escriure **nom o id** del Pokémon (ex: `pikachu` o `25`).
- Un botó **Cercar**.
- Un botó **Aleatori**.
- Un contenidor on es mostrarà el resultat.
- Un contenidor per mostrar errors (missatges clars per l'usuari).

### 2. Consum d’API amb `fetch`

Has de fer com a mínim **1 petició** a:

- `GET https://pokeapi.co/api/v2/pokemon/{nameOrId}`

Has d’usar:

- `async/await` o Promeses amb `.then()`.
- `try/catch` per capturar errors de xarxa.
- Gestió de `response.ok` (si no és OK, mostra error controlat).

### 3. Dades a mostrar (mínim)

Quan la consulta funcioni, mostra:

- **Nom** (en majúscula o amb format llegible)
- **ID**
- **Imatge** (sprite frontal) _(pista: `sprites.front_default`)_
- **Alçada i pes**
- **Tipus** (1 o 2)
- **Estadístiques bàsiques**: HP, Attack, Defense, Speed

### 4. Validació i errors

- Si l’input és buit: mostra "Introdueix un nom o id".
- Si no existeix el Pokémon (404): mostra "Pokémon no trobat".
- Si falla la xarxa: mostra “Error de connexió”.

## Tasques extra

1. **Llista d’habilitats**: mostra les abilities.
2. **Color del fons** segons el tipus principal (ex: `grass` verd, `water` blau).
3. **Navegació**: botons per veure el Pokémon anterior i següent (ID -1 i +1).

## Restriccions tècniques

- Prohibit usar llibreries (jQuery, Axios, frameworks).
- Codi en fitxers separats: `index.html`, `style.css`, `app.js`.

## Pistes

- Endpoint principal: `https://pokeapi.co/api/v2/pokemon/pikachu`
- Recorda: `fetch()` **no** llença error per 404; ho has de controlar amb `response.ok`.
- Normalitza l'entrada: `trim()` i `toLowerCase()` per noms.
