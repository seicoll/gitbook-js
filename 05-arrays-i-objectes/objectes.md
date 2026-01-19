# Objectes

## Què és un objecte?

- Un objecte és una col·lecció de propietats i valors. Cada propietat té un nom (clau) i un valor.
- Exemple:
  ```javascript
  let persona = {
    nom: "Anna",
    edat: 30,
    ciutat: "Barcelona",
  };
  console.log(persona);
  ```

## Accedir a les propietats

- Amb notació de punt:
  ```javascript
  console.log(persona.nom); // "Anna"
  console.log(persona.edat); // 30
  ```
- Amb notació de clau:
  ```javascript
  console.log(persona["ciutat"]); // "Barcelona"
  ```

## Afegir i modificar propietats

- Afegir:
  ```javascript
  persona.email = "anna@example.com";
  console.log(persona);
  ```
- Modificar:
  ```javascript
  persona.edat = 31;
  console.log(persona.edat); // 31
  ```

## Iterar sobre les propietats

- Amb `for...in`:
  ```javascript
  for (let clau in persona) {
    console.log(clau + ": " + persona[clau]);
  }
  ```

---

# Arrays d’objectes

- Un array pot contenir objectes.
- Exemple:
  ```javascript
  let persones = [
    { nom: "Anna", edat: 30 },
    { nom: "Joan", edat: 25 },
    { nom: "Maria", edat: 28 },
  ];
  console.log(persones[1].nom); // "Joan"
  ```

## Iterar sobre un array d’objectes

- Exemple:
  ```javascript
  persones.forEach(function (persona) {
    console.log(persona.nom + " té " + persona.edat + " anys.");
  });
  ```

## Exercicis Pràctics

1. **Crea i treballa amb objectes**:
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

2. **Arrays d’objectes**:
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
