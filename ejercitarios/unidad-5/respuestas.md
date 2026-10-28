# Respuestas — Ejercitario Unidad 05

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.
> Las imágenes (diagramas, capturas, wireframes) se suben a esta misma carpeta y se enlazan así: `![descripción](nombre-archivo.png)`

---
 
## Tema 1 · El diseño en la ingeniería de software

**1. Explica con tus palabras la diferencia entre diseño conceptual y diseño técnico (detallado). Da un ejemplo de una decisión de cada tipo para un sistema de gestión de una biblioteca.**

_Respuesta:_
**Diseño conceptual:** Es la etapa donde se define qué va a hacer el sistema a un alto nivel, enfocándose en los requerimientos del usuario, las entidades principales del negocio y su lógica general, sin preocuparse por la tecnología, lenguajes de programación o bases de datos específicas que se van a usar.

**Diseño técnico (detallado):** Es la etapa donde se define cómo se va a implementar lo anterior, especificando la tecnología exacta, estructuras de datos físicas, algoritmos, frameworks, protocolos de comunicación y componentes de hardware o software concretos. 

**Ejemplo para un sistema de gestión de una biblioteca:**

**Decisión conceptual:** Decidir que el sistema debe permitir registrar usuarios (socios) y asociarles un límite máximo de libros que pueden retirar simultáneamente.

**Decisión técnico (detallado):** Decidir que la tabla de socios se almacenará en una base de datos PostgreSQL utilizando una clave primaria de tipo UUID, y que la validación del límite de libros se hará mediante un procedimiento almacenado (stored procedure) en la base de datos.

**2. Completa el siguiente cuadro sobre los elementos del modelo de diseño.**

| Elemento del diseño | ¿Qué define? | Ejemplo en un sistema de inscripciones |
|---|---|---|
| Diseño de datos | La estructura, organización y representación de la información que la aplicación procesará, almacenará y manipulará. | Las tablas y relaciones en la base de datos para almacenar estudiantes, materias, cupos y actas de inscripción. |
| Diseño arquitectónico | La estructura global del sistema, organizándolo en componentes principales (capas o subsistemas) y cómo interactúan entre sí. | Definir una arquitectura de 3 capas: Presentación (pantallas web), Lógica de Negocio (reglas de inscripción) y Acceso a Datos. |
| Diseño de interfaces | Cómo interactúan los usuarios con el sistema (interfaz humana), cómo se comunican los subsistemas internos entre sí, y la interacción con sistemas externos. | El diseño de las pantallas y formularios web donde el alumno selecciona las materias y hace clic en "Inscribirse". |
| Diseño de componentes | La estructura interna y lógica de los módulos de software individuales (clases, funciones o servicios) que realizan tareas específicas. | El diseño detallado de la clase o servicio ValidadorDeCorrelativas, que verifica si el alumno aprobó las materias previas. |


---

## Tema 2 · Conceptos fundamentales de diseño

**3. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Concepto | Número |
|---|---|
| A. Abstracción | 4 |
| B. Refinamiento progresivo | 6 |
| C. Ocultamiento de información | 2 |
| D. Separación de intereses | 5 |
| E. Patrón | 3 |
| F. Refactorización | 1 |

1. Mejorar la estructura interna sin cambiar el comportamiento externo.
2. Cada módulo esconde sus decisiones internas y solo expone su interfaz.
3. Solución probada a un problema de diseño que se repite en un contexto dado.
4. Concentrarse en lo esencial e ignorar los detalles irrelevantes en ese nivel.
5. Dividir un problema en partes que se puedan resolver y modificar de forma independiente.
6. Agregar detalle en pasos sucesivos, partiendo de una descripción general.

**4. Aplica refinamiento progresivo a la tarea "Registrar una venta en un comercio": escribí al menos tres niveles de detalle, refinando en el tercer nivel uno de los pasos del segundo.**

_Respuesta:_
**Nivel 1 (Descripción general):**

1- Registrar una venta en el comercio.

**Nivel 2 (Primer desglose de pasos):**

1- Escanear o ingresar los productos seleccionados por el cliente.

2- Calcular el total a pagar aplicando impuestos y descuentos si corresponden.

3- Procesar el pago (efectivo, tarjeta o transferencia).

4- Generar y entregar el comprobante de venta.

**Nivel 3 (Refinando el paso 3 del nivel anterior: "Procesar el pago"):**

1- Solicitar al cliente el medio de pago deseado.

2- Si es con tarjeta: conectar con la pasarela de pagos, solicitar PIN o lectura contactless, y esperar la autorización del banco.

3- Si es en efectivo: ingresar el monto recibido, calcular el vuelto y abrir la caja registradora.

4- Registrar la transacción exitosa en el sistema de caja.


## Tema 3 · Descomposición y modularidad

**5.Explica por qué no conviene dividir un sistema ni en muy pocos ni en demasiados módulos. ¿Qué costos aumentan en cada extremo?**

No conviene irse a los extremos porque se afecta directamente la complejidad y el mantenimiento del software:

**Demasiado pocos módulos (Módulos gigantes o monolíticos):** El sistema se divide en pocas partes pero muy grandes. Aumentan los costos de mantenibilidad y comprensión, ya que cada módulo hace demasiadas cosas (baja cohesión), haciendo que sea difícil de entender, probar o modificar sin romper otra funcionalidad.

**Demasiados módulos (Exceso de fragmentación):** El sistema se divide en una infinidad de piezas diminutas. Aumentan los costos de integración y coordinación, ya que hay que gestionar una gran cantidad de dependencias, llamadas y comunicación entre módulos, lo que vuelve el sistema excesivamente complejo de ensamblar y depurar.
**6. Para un sistema de gestión de un consultorio médico, propone dos descomposiciones distintas e indica qué módulos tendría cada una.**

| Estrategia | Módulos propuestos |
| :--- | :--- |
| **Por capas** | 1. **Capa de Presentación:** Interfaz de usuario (web o app móvil para pacientes y secretarios).<br>2. **Capa de Lógica de Negocio:** Reglas de turnos, historias clínicas y validaciones de obras sociales.<br>3. **Capa de Acceso a Datos:** Conexión y persistencia con la base de datos del consultorio. |
| **Por dominio** | 1. **Módulo de Gestión de Pacientes:** Altas, bajas, modificaciones y datos de contacto.<br>2. **Módulo de Agenda y Turnos:** Reserva, cancelación y recordatorios de citas médicas.<br>3. **Módulo de Historia Clínica:** Registro de diagnósticos, recetas y evolución del paciente.<br>4. **Módulo de Facturación y Obras Sociales:** Cobros, bonos y liquidación a prepagas.|
---

## Tema 4 · Cohesión y acoplamiento

**7. Indica el tipo de cohesión de cada módulo (coincidental, lógica, temporal, procedimental, comunicacional, secuencial o funcional) y justifica brevemente.**

| Módulo | Tipo de cohesión y justificación |
|---|---|
| a) "Utilidades": FormatearFecha, EnviarCorreo y CalcularIVA. | Coincidental: realiza tareas diferentes que no están relacionadas entre sí. |
| b) "IniciarSistema": abre la conexión a la base, carga la configuración y borra archivos temporales. | Temporal: agrupa tareas que se realizan al iniciar el sistema. |
| c) "CalcularPromedioAlumno": obtiene las notas de un alumno y devuelve su promedio. | Funcional: todas las operaciones tienen el mismo objetivo: calcular el promedio del alumno. |
| d) "ProcesarOperacion": recibe un código y, según su valor, imprime, guarda o elimina un registro. | Lógica: agrupa operaciones similares y elige cuál ejecutar según un código. |
| e) Lee un registro, lo valida y, con el registro ya validado, calcula su total. | Secuencial: la salida de una operación sirve como entrada para la siguiente. |

**8. Indica el tipo de acoplamiento en cada caso (de datos, por estampado, de control, externo, común o de contenido).**

| Situación | Tipo de acoplamiento |
|---|---|
| a) El módulo A llama a B pasándole solo el idAlumno. | De datos: se pasan únicamente los datos necesarios. |
| b) A le pasa a B una bandera modo = "imprimir" / "guardar" que decide qué hace B. | De control: un parámetro determina el comportamiento del otro módulo. |
| c) Varios módulos leen y modifican la variable global TotalVentas. | Común: comparten una variable global. |
| d) A modifica directamente un atributo privado de B. | De contenido: un módulo accede o modifica directamente el interior de otro. |
| e) A le pasa a B el objeto Alumno completo, aunque B solo usa la fecha de nacimiento. | Por estampado: se pasa una estructura completa aunque solo se necesita una parte. |

**9. Explica por qué la alta cohesión y el bajo acoplamiento suelen ir de la mano. Da un ejemplo.**

_Respuesta:_
La alta cohesión significa que un módulo se encarga de una tarea específica, mientras que el bajo acoplamiento significa que depende poco de otros módulos. Ambos facilitan el mantenimiento y los cambios del sistema.

Ejemplo: un módulo que calcula promedios solo se encarga de esa tarea y recibe las notas como parámetros, sin depender de otros módulos ni modificar sus datos internos.

---

## Tema 5 · Arquitectura y estilos arquitectónicos clásicos

**10. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Estilo arquitectónico | Número |
|---|---|
| A. En capas | _5_ |
| B. Cliente-servidor | _4_ |
| C. Centrado en datos (repositorio) | _2_ |
| D. Tuberías y filtros | _1_ |
| E. Modelo-Vista-Controlador | _3_ |

1. Un compilador: análisis léxico → sintáctico → semántico → generación de código.
2. Un entorno de desarrollo donde editor, depurador y analizador comparten un modelo central del proyecto.
3. Una aplicación web donde un controlador recibe el pedido, actualiza el modelo y elige qué vista mostrar.
4. Un cajero automático que consulta al servidor del banco para cada operación.
5. Un sistema contable organizado en presentación, lógica de negocio y acceso a datos.

**11. Dibujá o describí la arquitectura en capas de un sistema que conozcas (de tu trabajo, de la universidad o una app de uso diario), indicando la responsabilidad de cada capa. Si lo dibujan, agreguen la imagen al repositorio y enlácenla en la respuesta.**

_Respuesta:_


---

## Tema 6 · Estilos actuales y estrategia de selección

**12. Completa el siguiente cuadro comparativo.**

| Aspecto | Monolito modular | Microservicios |
|---|---|---|
| Despliegue | Se despliega como una única unidad (un solo archivo ejecutable o contenedor). Si cambia una línea, se republica toda la aplicación.  |  Despliegue independiente por cada servicio. Cada microservicio se actualiza por separado sin afectar a los demás.|
| Escalado | Se escala horizontalmente duplicando la aplicación entera (copias idénticas del monolito), lo que consume más recursos.  | Escalado granular y eficiente; se escalan únicamente aquellos servicios específicos que experimentan mayor demanda.  |
| Complejidad operativa | Baja o moderada. Requiere un solo repositorio, una sola base de datos y un pipeline de CI/CD sencillo.   | Alta. Requiere orquestadores (como Kubernetes), gestión distribuida de bases de datos, trazabilidad distribuida y redes complejas (Service Mesh).  |
| ¿Cuándo conviene? | En equipos pequeños, startups en fase temprana (MVP) o dominios de negocio donde la complejidad aún no justifica la distribución.  | En sistemas grandes con dominios bien acotados, equipos de desarrollo autónomos y una alta necesidad de escalado independiente y despliegue continuo. |

**13. Una empresa nueva con tres desarrolladores quiere empezar su producto directamente con quince microservicios. ¿Qué le recomendarías y por qué?**

_Respuesta:_ 
Les recomendaría rechazar los microservicios y optar por un Monolito Modular. Debido a que con un equipo de solo tres personas, la carga cognitiva y operativa de mantener quince microservicios sería insostenible. En lugar de escribir código de negocio, el equipo pasaría la mayor parte del tiempo configurando redes, infraestructura, contratos de API, descubrimiento de servicios y pipelines de despliegue. Un monolito modular les permite estructurar el código en dominios separados (preparándolos para el futuro) pero con la simplicidad de un único despliegue y una base de código centralizada.


**14. Para cada escenario, indica el atributo de calidad prioritario y un estilo arquitectónico que lo favorezca.**

| Escenario | Atributo prioritario | Estilo que lo favorece |
|---|---|---|
| Plataforma de venta de entradas con picos enormes de demanda al abrir la venta. | Escalabilidad | Microservicios (permite escalar horizontalmente solo el módulo de venta/pagos) o Arquitectura orientada a eventos. |
| Sistema bancario de transferencias entre cuentas. | Consistencia (Fiabilidad / Integridad transaccional / Correctitud) | Monolito modular (facilita transacciones ACID robustas) o Microservicios con patrones de Saga estrictos. |
| Sistema académico cuyas reglas de inscripción cambian cada semestre. | Mantenibilidad (Modificabilidad / Flexibilidad) | Arquitectura Limpia / Hexagonal o Monolito modular (permite aislar la lógica de negocio y cambiar reglas rápidamente sin propagar impactos) |


---

## Tema 7 · Características de un buen diseño

**15. Menciona las tres directrices de calidad de Pressman para un buen diseño y explica una de ellas con un ejemplo propio.**

_Respuesta:_
Las tres directrices de calidad de Roger Pressman para un buen diseño de software son:
- El diseño debe implementar todos los requisitos explícitos dados por el cliente y reflejar los requisitos implícitos deseados.
- El diseño debe ser una guía legible y comprensible para quienes construyen el código y para quienes lo van a probar y mantener.
- El diseño debe proporcionar una representación completa del software, abarcando desde la arquitectura global hasta los detalles de implementación de cada componente.

Ejemplo de la segunda directriz (Legibilidad y Comprensibilidad):
Imagina que diseñamos un sistema de comercio electrónico y nombramos a una función principal **calc_X_val()**. Aunque cumple con su tarea matemática, un nuevo desarrollador no entenderá qué calcula sin leer todo el código fuente. En cambio, si el diseño y los diagramas especifican nombres claros como **calcular_costo_envio_con_impuestos()**, el diseño se vuelve auto-documentado, comprensible y fácil de mantener.


**16. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Síntoma | Número |
|---|---|
| A. Rigidez | 3 |
| B. Fragilidad | 4 |
| C. Inmovilidad | 2 |
| D. Repetición innecesaria | 1 |

1. La misma lógica está copiada en varios lugares del sistema.
2. Cuesta reutilizar un componente porque arrastra demasiadas dependencias.
3. Un cambio simple obliga a modificar muchos módulos.
4. Un cambio rompe partes que aparentemente no tenían relación.


---

## Tema 8 · Principios SOLID

**17. Completa el cuadro con el nombre de cada principio y lo que propone, en una oración.**

| Letra | Principio | ¿Qué propone? |
|---|---|---|
| S | Responsabilidad única (Single Responsibility) | Una clase debe tener una única responsabilidad y una sola razón para cambiar |
| O | Abierto/Cerrado (Open/Closed) | Las clases deben estar abiertas a la extensión, pero cerradas a la modificación |
| L | Sustitución de Liskov (Liskov Substitution) | Una clase derivada debe poder sustituir a su clase base sin alterar el comportamiento esperado |
| I | Segregación de interfaces (Interface Segregation) | Es mejor tener interfaces pequeñas y específicas que obligar a una clase a implementar métodos que no necesita |
| D | Inversión de dependencias (Dependency Inversion) | Los módulos de alto nivel deben depender de abstracciones y no directamente de implementaciones concretas |

**18. Analiza la siguiente clase: "ReporteVentas obtiene las ventas desde SQL Server, calcula los totales, arma un PDF y lo envía por correo". ¿Qué principio SOLID viola principalmente? Propone una mejor distribución de responsabilidades (nombres de clases o interfaces y qué hace cada una).**

_Respuesta:_ El principio que viola principalmente es el Principio de Responsabilidad Única (SRP), porque la clase realiza demasiadas tareas diferentes: consulta la base de datos, calcula totales, genera un PDF y envía correos. Por lo tanto, tiene varias razones para cambiar.

---

## Tema 9 · Evaluación y validación del diseño

**19. Explica la diferencia entre una revisión técnica del diseño y una prueba del software. ¿Por qué conviene revisar el diseño antes de programar?**

_Respuesta:_ Una revisión técnica del diseño consiste en analizar los documentos, diagramas y estructuras del sistema para detectar errores antes de programar. En cambio, una prueba del software consiste en ejecutar el programa para comprobar si funciona correctamente y cumple los requisitos.

Conviene revisar el diseño antes de programar porque permite detectar errores tempranamente, reducir costos de corrección y evitar problemas estructurales que serían más difíciles de solucionar después.


**20. Completa la matriz de trazabilidad para un sistema de biblioteca, indicando qué elementos de diseño (módulos, clases, interfaces, pantallas) satisfacen cada requerimiento.**

| Req. | Descripción | Elementos de diseño que lo satisfacen |
|---|---|---|
| RF-01 | Registrar el préstamo de un libro a un socio. | Módulo GestionPrestamos, clases Prestamo y PrestamoDAO, interfaz IPrestamoService y pantalla RegistrarPrestamo |
| RF-02 | Avisar por correo al socio cuando vence un préstamo. | Módulo Notificaciones, clases ServicioCorreo y Prestamo, interfaz I ServicioCorreo (o IEmailService) y tarea programada VerificarVencimientos |
| RF-03 | Buscar libros por título, autor o tema. | Módulo Catalogo, clases Libro y LibroDAO, interfaz IBusquedaLibros y pantalla BuscarLibros |
| RNF-01 | Solo el personal de la biblioteca puede registrar préstamos. | Módulo Seguridad, clases Autenticacion y Autorizacion, interfaz IAutorizacion y pantalla de inicio de sesión; control de permisos en el servicio de préstamos |


---

## Tema 10 · Diseño de la interfaz de usuario

**21. Para cada regla de oro, da un ejemplo de una aplicación o sitio que la cumpla y otro que la viole.**

| Regla de oro | Ejemplo que la cumple | Ejemplo que la viola |
|---|---|---|
| Dar el control al usuario | Gmail permite cancelar el envío de un correo durante unos segundos | Un sitio que abre ventanas emergentes constantemente sin permitir cerrarlas fácilmente |
| Reducir la carga de memoria | Una tienda online muestra el carrito y los productos seleccionados durante la compra | Un formulario que obliga al usuario a recordar datos de una pantalla anterior porque no los muestra ni los conserva |
| Lograr una interfaz consistente | Microsoft Word mantiene una disposición y unos controles similares en sus distintas herramientas | Una aplicación donde el botón «Guardar» cambia de ubicación y significado en cada pantalla |

**22. Realiza el análisis previo al diseño de la interfaz para la aplicación de autogestión de alumnos de la universidad.**

| Aspecto | Descripción |
|---|---|
| Usuarios | Alumnos de la universidad, con distintos niveles de experiencia tecnológica, y personal administrativo que brinda asistencia |
| Tareas principales | Consultar calificaciones, horarios, materias disponibles, inscribirse a asignaturas, verificar asistencia y descargar constancias |
| Entorno de uso | Computadoras y teléfonos móviles, desde el hogar, la universidad o cualquier lugar con conexión a internet. Puede haber usuarios con conexiones lentas o pantallas pequeñas |


---

## Tema 11 · Usabilidad, accesibilidad y prototipos

**23. Evaluación heurística: elijan una pantalla real (de un sitio web o una app que usen), agreguen una captura al repositorio e identifiquen al menos tres problemas de usabilidad o accesibilidad.**

| Problema detectado | Heurística de Nielsen violada | Mejora propuesta |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |

**24. Elijan una pantalla clave del sistema de su Trabajo Práctico y dibujen su wireframe (puede ser la foto de un boceto en papel, agregada al repositorio). Indiquen qué regla de oro o heurística tuvieron en cuenta en al menos dos decisiones.**

_Respuesta:_


**25. Reflexión final: ¿qué estilo arquitectónico proponen para el sistema de su Trabajo Práctico y por qué? Justifiquen la elección con al menos dos atributos de calidad del sistema.**

_Respuesta:_

