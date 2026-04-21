# Introducció a TypeScript

## Què és TypeScript?

* **TypeScript (TS)** és un llenguatge de programació de codi obert desenvolupat per Microsoft que es basa en JavaScript. 
  
* És un **superconjunt de JavaScript (JS)**, el que significa que tot el codi JavaScript és també codi TypeScript vàlid. 
  
* La principal característica de TypeScript és que afegeix **tipatge** estàtic al llenguatge, permetent als desenvolupadors definir tipus per a variables, funcions i altres estructures de dades.
    * Això ajuda a detectar errors en temps de compilació, abans que el codi s'executi, millorant la qualitat i mantenibilitat del codi.

**AFEGIR ALGUNS VIDEOS:**
* [TypeScript in 100 Seconds](https://www.youtube.com/watch?v=BCg4U1FzODs)
* [TypeScript Tutorial for Beginners](https://www.youtube.com/watch?v=BwuLxu7C9kU)

## Superconjunt i transpilació

### Superconjunt

* **TS** inclou tota la sintaxi i la funcionalitat **de** JS. Qualsevol fitxer `.js` pot reanomenat a `.ts` i, en principi, hauria de funcionar sense problemes.

### Transpilació
* Els **navegadors** només entenen JS.
* El codi TypeScript no s'executa directament en els navegadors. Per tant, es necessita un procés de **transpilació** per convertir el codi TypeScript en JavaScript que els navegadors poden interpretar.
* Aquesta **transpilació** es realitza mitjançant  una eina de línia de comandes `tsc` (**TypeScript Compiler**) o altres eines com Webpack, Babel, etc.