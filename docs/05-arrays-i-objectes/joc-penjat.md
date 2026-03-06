# Joc del penjat

Aquesta activitat consisteix a realitzar el joc del penjat en Javascript.

![](hangman.jpg)

En la pàgina hi ha de sortir:

- Una zona on ha d'aparèixer el nombre d'**espais** corresponent al nombre de lletres que conté la paraula.
- Una zona amb la **imatge del penjat**, en cas que l’usuari falli una lletra de la paraula es mostrarà una nova part d’aquesta imatge.
- Una altra zona de la pàgina on apareixen totes les **lletres de l'abecedari** i es pot clicar per utilitzar-les.

## Requeriments

- Les paraules a endevinar hauran d'estar prefixades i emmagatzemades en l’aplicació.
- Cal fer servir events del teclat per anar marcant cada lletra.
- Mostrar l’abecedari en pantalla i poder clicar sobre les lletres
- Al utilitzar una lletra cal que la marqueu com a afegida en l’abecedari.
- En cas de ser una lletra de la paraula, caldrà que aparegui sobre l’espai corresponent de la paraula.
- En cas que no estigui dins de la paraula, aquesta serà un error a comptabilitzar i caldrà mostrar la part del ninot del penjat.
- El resultat haurà de determinar si l’usuari ha guanyat o no.

## Valoració de la pràctica

- Funcionament del joc. **[2.5 punts]**
- Poder triar una lletra prement les tecles del teclat. **[1 punt]**
- Controlar que no es repeteixi una lletra ja utilitzada. **[0.5 punts]**
- Mostrar totes les lletres de l’abecedari a la pantalla i poder triar una lletra clicant a sobre. **[1 punt]**
- Marcar d’estil diferent les lletres ja utilitzades. **[0.5 punts]**
- Definir un nombre màxim d’errades i mostrar una nova part de la imatge del penjat cada lletra errada. **[2 punts]**
- Valoració del disseny joc (botó nova partida, colors, tipus de lletra, etc) **[1 punt]**
- Limitar el temps del joc utilitzant un compte enrere. **[1 punt]**
- Codi Javascript correctament tabulat i comentat. **[0.5 punts]**

L'estructura general del programa potser alguna cosa així:

```javascript
//Array amb les possibles paraules a endevinar al joc
let paraules = [...];

//Paraula a endevinar
let paraula;

// Nombre de fallades festes per saber quina imatge del penjat cal mostrar
let errades;

// arrayResposta tindrà el procés de la paraula que anem endevinant
let arrayResposta = [];

function inicialitzarJoc(){
  //Seleccionem una paraula a l’atzar de dins l’array paraules
  paraula = ...

  //Inicialitzem l'array resposta [_ _ _ _ _]
  …

  //Inicialitzem les errades a 0
  errades = 0;

  //Actualitzem la interfície mostrant l'estat actual de la paraula a endevinar
  pintarParaula(arrayResposta);

}


function comprovarLletra(lletra)
{

  //Comprovar si la lletra està dins de la paraula a endevinar
  if (...) {
      //Si la lletra està dins de la paraula

      //Actualitzar l'arrayResposta amb la lletra
      pintarPaurla(arrayResposta);
  } else {
      //Si la lletra no està dins de la paraula

      //Incrementar el nombre d'errades

      //Canviar la imatge del penjat mostrada
  }
}
```

**Exemple de com detectar les lletres apretades del teclat:**
[https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_event_key_keycode2](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_event_key_keycode2)
