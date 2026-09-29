---
title: "Conceptualización"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 1 · Conceptualización.

---
En la actualidad, la "Mini Farmacia Familiar" administrada por la señora Doris gestiona todos sus procesos operativos, como el registro de ventas y el control de inventario, de manera íntegramente manual mediante el uso de cuadernos y planillas físicas. Esta metodología de trabajo genera una problemática concreta: la incapacidad de mantener un control preciso y en tiempo real de los productos. Como consecuencias observables de esta situación, el negocio experimenta una notable lentitud en la atención en el mostrador, discrepancias recurrentes en el arqueo de caja diario y, de manera crítica, pérdidas económicas ocasionadas por el vencimiento de medicamentos en los estantes al no existir un seguimiento estricto de sus fechas de caducidad.
## 1. Presentación del proyecto

**Nombre del sistema:** FarmaClick.

**Integrantes del grupo:**

| Nombre | Rol |
|---|---|
| **Sofia Esther Vargas Vallejos** | **Desarrollador Back-End :**  Crea la lógica del negocio, gestiona el servidor, diseña la base de datos y crea las APIs que el Front-end va a construir  |
| **Manuel Galeano**| **Desarrollador Front-End (UI/UX):** se encarga de todo lo que el usuario ve y con lo que interactúa. Construye la interfaz gráfica, (pantallas, botones, formularios) asegurando que el diseño sea responsivo e intuitivo.|
| **Milagros  Montserrat  Alcaraz Quiñonez** | **Líder de proyecto, DevOps:** coordina el trabajo usando metodologías agiles, organiza el repositorio en GitHub, resuelve bloqueos del equipo y configura el servidor, entorno donde vivirá el proyecto  |
| **Blas Ariel Benega López** |**Tester(QA)/ Documentador:** su misión es romper la aplicación antes de que se entregue. Realiza pruebas manuales y automatizadas para poder encontrar bugs, revisar que el código de sus compañeros este bien al desplegarse, y redactar manual técnico o la documentación del sistema. |

**Usuario / cliente real:** [nombre y breve descripción del usuario o cliente para quien se desarrolla el sistema]

---
Señora Doris, propietaria de la Mini Farmacia Familiar.
## 2. Definición del problema

[Describir la situación actual del usuario/cliente y la problemática concreta que motiva el desarrollo del sistema. ¿Qué hace hoy el usuario para resolver esto? ¿Qué dificultades enfrenta?]

---
**Situación actual:** Actualmente, la señora Doris registra las ventas diarias y el control de su mercadería utilizando cuadernos y planillas manuales.   
**Problemática concreta:** El registro manual provoca lentitud en la atención al cliente, errores de cálculo en la caja diaria y, lo más grave, el desconocimiento del stock real. Esto genera que productos se agoten sin previo aviso o que los medicamentos expiren en los estantes sin ser detectados a tiempo.
## 3. Propósito y objetivos

[Redactar en una frase el objetivo general del sistema.]
**Objetivo general:** Desarrollar un sistema informático que permita gestionar el inventario y registrar las ventas de la mini farmacia de la señora Doris de forma rápida y centralizada. 


**Objetivos específicos:** 

1. Registrar las ventas diarias calculando automáticamente el total a cobrar y el vuelto.     
2. Gestionar el inventario de medicamentos, actualizando el stock con cada venta.
3. Generar reportes de los medicamentos que están próximos a su fecha de vencimiento.

---

## 4. Alcance del proyecto

**Incluye (dentro del alcance):**

- Incluido en la primera versión: Módulo de registro de medicamentos (altas, bajas y modificaciones), módulo de punto de venta (facturación interna) y alertas de bajo stock o vencimiento. 

**No incluye (fuera de alcance):**
---

- Fuera de alcance: El sistema no incluirá facturación electrónica legal con la SET, no tendrá tienda online para envíos a domicilio, ni módulo de pago con tarjetas integrado directamente en el software (se usará POS externo).   



## 5. Interesados (stakeholders)

| Interesado | Descripción | Interés en el proyecto |
|---|---|---|
| La señora Doris y/o encargado | La señora Doris y/o el personal encargado de la atención al mostrador en la farmacia. | Esperan una interfaz rápida, intuitiva y muy fácil de usar para registrar ventas y buscar precios sin hacer esperar a los clientes. |
| La  señora  Doris  | La señora Doris (Propietaria de la "Mini Farmacia Familiar").| Busca tener el control exacto de su inventario, reducir las pérdidas económicas por medicamentos vencidos y conocer sus ingresos diarios. |
| Administrador del proyecto| El equipo de desarrollo del proyecto o la persona designada para dar soporte técnico. | Esperan un sistema estable, con código limpio que sea fácil de mantener y actualizar, además de poder gestionar copias de seguridad sin complicaciones. |

---

## 6. Justificación / viabilidad

**Viabilidad técnica:** El equipo cuenta con los conocimientos necesarios en lenguajes de programación web/escritorio para desarrollarlo.

**Viabilidad operativa:** La interfaz se diseñará con botones grandes y flujos sencillos, asegurando que Doris pueda utilizarlo sin conocimientos técnicos avanzados.

**Viabilidad económica (alto nivel):** [Al utilizar herramientas de código abierto y un servidor local o gratuito, los costos de desarrollo e implementación serán mínimos o nulos para la farmacia.
---

## 7. Visión general de la solución

El sistema será una aplicación que permitirá buscar medicamentos por nombre de forma rápida. Al confirmar una venta, el sistema restará automáticamente los productos del inventario y guardará el registro para que, al final del día, la señora Doris pueda ver cuánto dinero ingresó y qué productos necesitan ser reabastecidos.
## 8. Glosario de términos

| Término | Definición |
|---|---|
|**Principio Activo:**| Componente principal del medicamento (ej. Paracetamol).|
|**Lote:** | Código de identificación de un grupo de medicamentos producidos en la misma fecha.|
| **Stock Mínimo:**| Cantidad límite de un producto que indica que es momento de volver a comprarle al proveedor. |

---

## 9. Riesgos iniciales

| Riesgo | Impacto | Estrategia de mitigación |
|---|---|---|
| Baja disponibilidad del cliente para validaciones: Tiempo limitado de la señora Doris para atender al equipo debido a la atención continua de su negocio. | Alto|Coordinar reuniones breves de máximo 20 minutos en horarios con poco movimiento en la farmacia, enviar prototipos visuales concretos y usar comunicación asincrónica por mensajes para dudas puntuales.|
| Resistencia al cambio o dificultad de uso: Posible complejidad en la curva de aprendizaje del cliente para adaptarse de cuadernos de papel a un software. | Alto  | Diseñar una interfaz extremadamente simple con botones claros y flujos cortos, realizar capacitaciones prácticas presenciales y entregar una guía de usuario visual paso a paso.|
| Datos de inventario desordenados o incompletos: Registros manuales previos inconsistentes (nombres ambiguos, precios desactualizados o faltantes de lotes/vencimientos).| Medio  | Entregar a la señora Doris una plantilla estándar sencilla para la carga inicial y dedicar una sesión previa con el equipo para organizar y unificar los datos antes de ingresarlos al sistema.|
| Retraso en el cronograma por sobrealcance: Intentar abarcar demasiadas funciones avanzadas y no llegar a tiempo con los plazos de la materia. | Medio  | Priorizar estrictamente el Módulo de Ventas e Inventario (Producto Mínimo Viable) en las primeras fases y mover las funciones secundarias a una lista de pendientes para etapas posteriores.|
---

## 10. Selección tecnológica preliminar

| Componente | Elección | Justificación breve |
|---|---|---|
| Lenguaje de programación |JavaScript | Permite usar un mismo lenguaje tanto en el cliente como en el servidor, agilizando el desarrollo y contando con una amplia variedad de librerías para la gestión de datos. |
| Framework | React (Front-end) + Node.js con Express (Back-end)| Permite construir una interfaz rápida, dinámica e intuitiva para las ventas en el mostrador, junto con un servidor liviano y eficiente para procesar las consultas del inventario.|
| Base de datos | PostgreSQL (o MySQL)| Es un motor relacional gratuito y robusto que garantiza la integridad y consistencia de los datos (inventario, precios y ventas) mediante transacciones seguras. |

---

[← Volver al inicio](index.md) · [Siguiente: Análisis →](analisis.md)
