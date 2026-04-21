# Tipatge de dades

* El tipatge de dades en TypeScript implica **especificar explícitament el tipus de dades** de les variables, els paràmetres de les funcions i els valors de retorn. 
* Això permet que la **verificació de tipus** estàtics de TS detecti errors durant la compilació. 
* Això millora la **qualitat** i el **manteniment** del codi.

## Tipus de dades bàsics
* Les anotacions dels tipus s'escriuen utilitzant els dos punts **`:`** seguits del tipus de dades.
  
* **Exemples**:
    ```typescript
    let nom: string = "David";
    let edat: number = 30;  
    function suma(a: number, b: number): number {
    return a + b;
    }
    ```

## Tipus de dades avançats
* TypeScript també admet tipus més avançats com **arrays**, **tuples**, **enums**, **void**, etc.
  
* Els **arrays** es poden tipar de la següent manera:
    ```typescript
    let nombres: number[] = [1, 2, 3];
    let noms: Array<string> = ["Alice", "Bob", "Charlie"];
    ```
* Les **tuples** permeten definir un array amb un nombre fix de elements i tipus específics per a cada element:
    ```typescript   
    let persona: [string, number] = ["David", 30];
    ``` 
## Unió de tipus

* La **Unió** `|` permet que una variable tingui un de diversos tipus definits.


    ```typescript
    // Una variable pot ser 'string' o 'number'
    let id: string | number; 

    id = "A123";  // Correcte
    id = 456;     // Correcte
    // id = true; // Error
    ```

## Tipus personalitzats
* TypeScript permet crear **tipus personalitzats**.

* Per **exemple**, es pot definir un tipus per representar els dies de la setmana:
  
    ```typescript
    type Dia = "dilluns" | "dimarts" | "dimecres" | "dijous" | "divendres";

    let dia: Dia;
    dia = "dimarts";  // Correcte
    dia = "juny";     // Incorrecte
    ```
    