# AJAX

> **AJAX** \(**A**synchronous **J**avaScript **A**nd **X**ML\) és un tècnica que permet comunicar-se amb el servidor i actualizar el contingut d'una pàgina web sense haver de recarregar tota la pàgina.

En les **aplicacions web tradicionals:**

1. Les accions de l'usuari \(clicar un enllaç, enviar formulari, etc.\) desencadenen crides al servidor. 
2. Un cop processada la petició de l'usuari, **el servidor retorna una nova pàgina** HTML al navegador de l'usuari.
3. En realitzar peticions contínues al servidor, l'usuari ha d'**esperar que es recarregui la pàgina** amb els canvis sol·licitats i això pot resultar molest.

**AJAX** permet millorar la interacció de l'usuari modificant part de la pàgina sense haver de recarregar la pàgina completament.

1. L'**intercanvi d'informació** amb el servidor l’executa el Javascript fent una petició AJAX en un segon pla.
2. Un cop es rep la resposta del servidor, es canvien **únicament les parts necessàries** de la pàgina.

![](../.gitbook/assets/ajax_logo.jpg)

### **Funcionament d’una aplicació AJAX**

1r. Un esdeveniment desencadena la necessitat de sol·licitar informació al servidor.

2n. Instanciar l’objecte XMLHttpRequest que en ens proporciona funcionalitat necessària per enviar i rebre informació de forma asíncrona.

3r. Preparar la funció de resposta que s’encarregarà de processar la informació de resposta del servidor.

4t. Crear la petició a servidor.

5è. Enviament de la petició al servidor.

6è. Executar la funció de resposta.  


\*\*\*\*

