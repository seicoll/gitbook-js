# Exercicis Pràctics

1. **Treballa amb arrays**:
   Escriu un programa que afegeixi i elimini elements d’un array:

   ```javascript
   let colors = ["vermell", "blau", "verd"];
   colors.push("groc"); // Afegir groc
   colors.shift(); // Treure el primer element
   console.log(colors);
   ```

2. **Filtra un array**:
   Escriu un programa que seleccioni només els nombres parells d’un array:

   ```javascript
   let nombres = [1, 2, 3, 4, 5, 6];
   let parells = nombres.filter(function (nombre) {
     return nombre % 2 === 0;
   });
   console.log(parells); // [2, 4, 6]
   ```

3. **Crea i treballa amb objectes**:
   Escriu un programa que mostri les propietats i valors d’un objecte:

   ```javascript
   let cotxe = {
     marca: "Toyota",
     model: "Corolla",
     any: 2021,
   };

   for (let clau in cotxe) {
     console.log(clau + ": " + cotxe[clau]);
   }
   ```

4. **Arrays d’objectes**:
   Escriu un programa que mostri els noms de persones d’un array d’objectes:

   ```javascript
   let alumnes = [
     { nom: "Pau", curs: "Matemàtiques" },
     { nom: "Laura", curs: "Física" },
     { nom: "Marta", curs: "Química" },
   ];

   alumnes.forEach(function (alumne) {
     console.log(alumne.nom + " estudia " + alumne.curs);
   });
   ```

---

## Tasca per fer a casa

1. Crea un array amb 5 números i calcula la suma total dels elements.
2. Crea un objecte que representi un llibre amb propietats com `títol`, `autor` i `any`. Mostra les propietats amb un bucle.
3. Crea un array d’objectes que representin pel·lícules (amb títol i director) i mostra el nom del director de cada pel·lícula.
