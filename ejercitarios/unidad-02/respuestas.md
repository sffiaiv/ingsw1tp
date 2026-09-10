# Respuestas — Ejercitario Unidad 02

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · Propiedades de los sistemas.

**1. Define en tus propias palabras qué es un sistema y da un ejemplo distinto al utilizado en clase.**

_Respuesta:_
Un sistema es un conjunto de elementos interrelacionados que trabajan juntos para cumplir un objetivo común un ejemplo puede ser un sistema de riego automático de un jardín que tendría sensores de humedad, una válvula, una bomba de agua y un temporizador que, interrelacionados, logran mantener las plantas regadas sin intervención manual.

**2. Enumera los seis elementos de un sistema basado en computadora.**

_Respuesta:_
Los elementos de un sistema basado en computadora son: Software, Hardware, Personas, Base de datos, Documentación y Procedimientos.


**3. Piensa en un sistema cotidiano (por ejemplo, una biblioteca, un supermercado o un club deportivo) y completa la tabla con un ejemplo propio para cada propiedad.**

| Propiedad | Ejemplo en el sistema elegido |
|---|---|
| Jerarquía | El supermercado se divide en secciones (cajas, góndolas, depósito), y cada sección en subprocesos más chicos (una caja individual, un pasillo específico)|
| Límites (fronteras) | Todo lo que ocurre dentro del local —stock, ventas, personal— es parte del sistema; los proveedores externos o el clima no lo son, aunque lo puedan afectar|
| Interrelación de elementos | Las cajas dependen del sistema de stock para saber si hay producto disponible, y el stock depende de las ventas registradas en caja|
| Propiedades emergentes | La "experiencia de compra" (rapidez, orden, disponibilidad) surge de cómo interactúan juntos cajas, góndolas y personal — ningún elemento por sí solo la genera |

**4. Dentro del mismo sistema, identifica un posible subsistema y justifica por qué lo consideras tal.**

_Respuesta:_
El sistema de cajas registradoras sería un subsistema dentro del supermercado: tiene sus propios elementos (cajero, caja registradora, lector de códigos), su propio límite claro (procesa pagos) y cumple una función específica dentro del sistema mayor, pero a su vez se relaciona con otros subsistemas (stock, seguridad) para que el supermercado funcione como un todo.

---

## Tema 2 · Los sistemas y su entorno

**5. Elige un sistema de software que uses habitualmente e identifica: una entrada, una salida y un elemento de su entorno.**

| Elemento | Descripción en el sistema elegido |
|---|---|
| Sistema elegido | WhatsApp, aplicación que permite enviar y recibir mensajes, imágenes, videos y realizar llamadas. |
| Una entrada | Un mensaje de texto que el usuario escribe y envia. |
| Una salida | El mensaje recibido y mostrado en la pantalla del destinatario. |
| Un elemento del entorno | Internet, ya que permite que WhatsApp se comunique con sus servidores y con otros usuarios. |

**6. ¿El sistema que elegiste es abierto o cerrado? Justifica tu respuesta.**

_Respuesta:_
WhatsApp es un sistema abierto, porque interactúa constantemente con su entorno. Necesita de Internet, servidores y dispositivos para poder enviar y recibir información. 

**7. Explica con tus palabras qué es la retroalimentación (feedback) en un sistema y da un ejemplo.**

_Respuesta:_
Es la información que recibe un sistema sobre el resultado de una acción y que puede utilizarse para mejorar o modificar su funcionamiento.
**Ejemplo:** En WhatsApp, cuando enviamos un mensaje, aparece un simbolo de entrega y lectura. Esta información permite saber si el mensaje fue enviado, recibido o leído.


**8. Para el mismo sistema, menciona una restricción externa real que podría afectarlo, indicando si es organizacional, regulatoria o tecnológica.**

_Respuesta:_
Una restricción externa podría ser una falla o interrupción de Internet, que impediría enviar o recibir mensajes correctamente. Es una restricción tecnológica, porque depende de la infraestructura de comunicación necesaria para que WhatsApp funcione correctamente.


---

## Tema 3 · Modelado de sistemas

**9. Menciona dos razones por las cuales es útil modelar un sistema antes de construirlo.**

_Respuesta:_
- Permite comprender y representar como funcionará el sistema antes de desarrollarlo.
- Ayuda a detectar errores, problemas o necesidades antes de invertir tiempo y recursos en la construcción.

**10. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Nivel de visión | Descripción |
|---|---|
| A. Visión del mundo (worldview) | _3_ |
| B. Visión del dominio | _4_ |
| C. Visión del elemento | _1_ |
| D. Visión detallada | _2_ |

1. El sistema particular que se va a construir, dentro del dominio.
2. Los componentes internos del sistema: software, hardware, datos, etc.
3. El contexto global: todos los sistemas y organizaciones que interactúan.
4. El sector o área específica del negocio dentro de ese contexto.

**11. Explica la diferencia entre vista estructural y vista de comportamiento, y da un ejemplo de notación para cada una.**

_Respuesta:_
La vista estructural muestra como esta formado el sistema, sus componentes y las relaciones entre ellos. Un ejemplo de notación es el diagrama de clases UML.

La vista de comportamiento muestra como funciona el sistema, es decir, como cambian sus estados o como interactúan sus componentes a lo largo del tiempo. Un ejemplo es el diagrama de secuencia UML.

**12. Diagrama de contexto:** elige un sistema simple (por ejemplo, un cajero automático, una app de delivery) y dibujá un diagrama de contexto que muestre el sistema y al menos dos entidades externas con las que interactúa. Adjuntá la imagen acá abajo.

_(Arrastrá la imagen a este archivo desde el editor de GitHub para insertarla)_
<img width="1536" height="1024" alt="imagen" src="https://github.com/user-attachments/assets/27e69ae4-7ae7-4483-b57b-ed96a0d16b96" />


**13. ¿En qué situación elegirías usar simulación en lugar de un modelo estático? Da un ejemplo concreto.**

_Respuesta:_
Elegiría una simulación cuando sea necesario observar como se comporta un sistema a lo largo del tiempo o bajo diferentes situaciones.

Ejemplo: Simular el funcionamiento de un cajero automático para analizar que ocurre cuando llegan muchos clientes al mismo tiempo y determinar cuanto tiempo deben esperar. 

---

## Tema 4 · El proceso de Ingeniería de Sistemas

**14. Explica la diferencia entre Ingeniería de procesos de negocio e Ingeniería de producto, dando un ejemplo de cada una.**

_Respuesta:_
En la ingenieria de procesos lo que se busca optimizar son los metodos por los cuales se llega a un determinado producto o servicio, en cambio la Inegieria de Producto busca la manera de optener mejores y mayores cantidades de produccion de un bien o servicio.

**15. Ordena numéricamente (1 a 4) los siguientes pasos genéricos del proceso de Ingeniería de Sistemas, según la secuencia vista en clase.**

| N.º | Paso |
|---|---|
| 3| Especificación del sistema |
| 1 | Definición de necesidades 
| 4| Asignación de requisitos entre elementos |
| 2| Análisis de factibilidad |

**16. Reflexión final:** ¿por qué crees que es importante que un ingeniero de software comprenda el sistema completo (Ingeniería de Sistemas) antes de comenzar a programar? Relaciona tu respuesta con algún ejemplo visto en la Unidad 01 o en esta unidad.

_Respuesta:_ 
El ingeniero de software debe tener una comprensión general del sistema ya que no solo se trata de desarrollar software sino lidiar con personas, clientes, jefes entre otros casos como por ejemplo el manejo de datos delicados como información medica, o información bancaria. El ingeniero de software no solo trabaja con herramientas tecnológicas, también trabaja con personas físicas y problemas de la vida real.
