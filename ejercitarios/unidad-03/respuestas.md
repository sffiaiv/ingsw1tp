# Respuestas — Ejercitario Unidad 03

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · El significado de proceso

**1. Define en tus propias palabras qué es un proceso de software.**

_Respuesta:_
Un proceso de software es el conjunto de pasos y actividades que se siguen para crear, desarrollar, probar, mantener y mejorar un programa o sistema de software.


**2. Explica la diferencia entre proceso, metodología y modelo de proceso, con un ejemplo de cada uno.**

_Respuesta:_
Un proceso es el conjunto de pasos para desarrollar un software, por ejemplo: analizar, diseñar, programar y probar. Una metodología es la forma de organizar y realizar esos pasos, como Scrum. Un modelo de proceso muestra cómo se ordenan las etapas, como el modelo en cascada, donde cada etapa se realiza en orden.


**3. Enumera las cinco actividades genéricas del marco de trabajo de Pressman.**

_Respuesta:_
1. Comunicación.
2. Planeación.
3. Modelado.
4. Construcción.
5. Despliegue.



**4. Menciona dos actividades "de la sombrilla" y explica por qué se dice que "cubren" todo el proceso.**

_Respuesta:_
Dos actividades de la sombrilla son gestión de riesgos y aseguramiento de la calidad. Se llaman así porque están presentes durante todo el proceso de desarrollo, desde el inicio hasta la entrega del software, y ayudan a controlar los riesgos y mantener la calidad.

---

## Tema 2 · Modelos de proceso

**5. Completen el siguiente cuadro indicando en qué situación conviene usar cada modelo de proceso visto en clase.**

| Modelo | ¿Cuándo conviene usarlo? |
|---|---|
| Cascada | Cuando los requisitos están claros y no se esperan muchos cambios. |
| Incremental |  Cuando se quiere entregar el sistema por partes y agregar funciones poco a poco. |
| Evolutivo (prototipos) | Cuando los requisitos no están claros y se necesita probar una versión inicial. |
| Evolutivo (espiral) | Cuando el proyecto es grande y tiene muchos riesgos que deben analizarse. |
| Concurrente | Cuando varias actividades se pueden realizar al mismo tiempo y se necesita avanzar rápidamente. |

**6. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Modelo de proceso | Característica principal |
|---|---|
| A. Cascada | 2 |
| B. Incremental | 4 |
| C. Prototipos | 5 |
| D. Espiral | 1 |
| E. Concurrente | 3 |

1. Combina iteración con análisis explícito de riesgo en cada vuelta.
2. Enfoque secuencial y lineal, actividad por actividad.
3. Representa actividades ocurriendo en paralelo, no en secuencia estricta.
4. Entrega el producto en porciones funcionales cada vez más completas.
5. Construye una versión parcial y rápida para validar requisitos poco claros.

**7. Elegí un proyecto de software (hipotético o real) y justificá qué modelo de proceso usarías para desarrollarlo y por qué.**

_Respuesta:_
Elegiría un sistema de gestión de biblioteca y utilizaría el modelo incremental, porque permite desarrollar el sistema por partes, por ejemplo: primero el registro de usuarios, luego el préstamo y devolución de libros y finalmente las consultas. Así se puede probar cada parte y mejorarla antes de completar todo el sistema.

---

## Tema 3 · Iteración de procesos

**8. Explica con tus palabras por qué la mayoría de los procesos modernos son iterativos.**

_Respuesta:_
Porque permiten desarrollar el software poco a poco, revisando y mejorando cada versión según los resultados y las necesidades del usuario.

**9. Menciona una ventaja y una desventaja de trabajar con iteraciones cortas.**

_Respuesta:_
Ventaja: Permiten detectar y corregir errores rapidamente.
Desventaja: Requiere una revisión constante y pueden generar mas trabajo de seguimiento.

---

## Tema 4 · Especificación, diseño, implementación, validación y evolución

**10. Describan brevemente qué implica cada una de las cuatro actividades fundamentales del proceso de software, según Sommerville.**

| Actividad | Qué implica |
|---|---|
| Especificación | Definir que debe hacer el sistema y cuáles son sus requisitos. |
| Diseño e implementación | Diseñar la solución y programar el sistema. |
| Validación | Comprobar que el sistema funciona correctamente y cumple los requisitos. |
| Evolución | Modificar y mejorar el sistema según nuevas necesidades. |

**11. Relaciona estas cuatro actividades con las cinco fases del ciclo del software vistas en la Unidad 1 (análisis, diseño, implementación, pruebas, mantenimiento). ¿En qué se parecen y en qué se diferencian?**

_Respuesta:_
---
 Las cuatro actividades de Sommerville se pueden relacionar así: la especificación corresponde al análisis, el diseño e implementación abarca tanto el diseño como la implementación del ciclo de vida, la validación equivale a las pruebas y la evolución corresponde al mantenimiento. Se parecen en que ambos modelos cubren las mismas etapas generales del desarrollo de un sistema. Se diferencian en que Sommerville agrupa diseño e implementación en una sola actividad, mientras que el ciclo de vida de la Unidad 1 las trata como fases separadas.
## Tema 5 · Herramientas y técnicas para modelado de procesos

**12. Menciona dos formas de representar un proceso (no un sistema) y explica brevemente cada una.**

_Respuesta:_
Una forma es el diagrama de flujo, que muestra las actividades del proceso y el orden en que se ejecutan mediante flechas y símbolos. Otra forma es la descripción narrativa o textual, donde se explica con palabras cada etapa del proceso, sus entradas, salidas y quién es responsable de cada una.

**13. ¿Qué es un patrón de proceso? Da un ejemplo hipotético de un problema recurrente en un proyecto y su solución.**

_Respuesta:_

---
Un patrón de proceso es una descripción de un problema que suele repetirse en distintos proyectos de software, junto con una solución probada para ese problema, de forma que se pueda reutilizar cuando vuelva a presentarse la misma situación. Por ejemplo, si en un proyecto los requisitos cambian constantemente y esto retrasa el desarrollo, se puede aplicar el patrón de "requisitos inestables", cuya solución sería adoptar un modelo de proceso incremental que permita ir ajustando el sistema en cada entrega sin tener que rehacer todo el trabajo.
## Tema 6 · Ayuda automatizada al proceso

**14. Explica la diferencia entre herramientas Upper-CASE y Lower-CASE.**

_Respuesta:_ una herramienta Upper-CASE se centra principalmente en las fases iniciales de un proyecto como las fases de planificacion, analisis, requisitos y diseños, mientras que una herramienta Lower-CASE se centra en las fases finales como construccion, generacion de codigo, pruebas e implementacion.
Podemos decir que una Upper-CASE se centra en Front-end y Lower-CASE se centra en Back-end.


**15. Menciona tres herramientas que consideren CASE (de su propia experiencia o investigación) y clasifíquenlas según la categoría a la que pertenecen.**

| Herramienta | Categoría (Upper / Lower / I-CASE) |
|---|---|
|PowerDesigner: modelacion y diseño de datos | Upper-CASE |
|EclipseIDE: codificacion, depuracion y pruebas| Lower-CASE |
|IBM Rational Software Architect: ciclo de vida, modelacion UML | I-CASE |

**16. Reflexión final:** de los modelos de proceso vistos en esta unidad, ¿cuál elegirían para un proyecto personal? Justifiquen su elección considerando el tamaño del proyecto, el tiempo disponible y el nivel de certeza sobre los requisitos.

_Respuesta:_
Desde experiencia personal, utilizaría Eclipse para un proyecto de programación usando Java ya que es una herramienta altamente funcional con posibilidad de integración de otros programas y funcionalidades, permitiendo pruebas de integracion y depuracion, asi como prueba de funcionalidades generales del sistema desarrollado 
