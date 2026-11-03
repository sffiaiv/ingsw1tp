---
title: "Análisis"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 2 · Análisis

> *Qué debe hacer el sistema, desde la perspectiva del negocio y del usuario.*

---

## 1. Requisitos funcionales

| ID | Requisito | Prioridad |
|---|---|---|
| RF-01 | El sistema debe permitir registrar, modificar, consultar y dar de baja medicamentos (CRUD), gestionando nombre comercial, principio activo, lote, precio de venta, stock actual, stock mínimo y fecha de vencimiento[cite: 1]. | Alta |
| RF-02 | El sistema debe permitir buscar productos rápidamente por nombre o principio activo y agregarlos al carrito de compra en el módulo de punto de venta[cite: 1]. | Alta |
| RF-03 | El sistema debe calcular automáticamente el total a cobrar y el vuelto según el monto entregado por el cliente[cite: 1]. | Alta |
| RF-04 | El sistema debe descontar de forma automática las cantidades correspondientes del inventario general al confirmar una venta[cite: 1]. | Alta |
| RF-05 | El sistema debe mostrar un aviso visual o alerta cuando un producto alcance o baje de su stock mínimo preestablecido[cite: 1]. | Media |
| RF-06 | El sistema debe generar un reporte o listado de alerta con los medicamentos próximos a su fecha de caducidad[cite: 1]. | Media |
| RF-07 | El sistema debe permitir generar un resumen del total de ingresos monetarios obtenidos en el cierre de caja diario[cite: 1]. | Baja |

---

## 2. Requisitos no funcionales

| ID | Requisito | Categoría |
|---|---|---|
| RNF-01 | Las consultas de búsqueda de medicamentos en el mostrador y el registro de ventas deben completarse en menos de 2 segundos[cite: 1]. | Rendimiento |
| RNF-02 | El acceso a las funciones administrativas (modificación de precios y gestión de inventario) requerirá autenticación básica de usuario[cite: 1]. | Seguridad |
| RNF-03 | La interfaz gráfica debe ser intuitiva, con botones grandes y flujos cortos, permitiendo su uso sin requerir conocimientos técnicos avanzados[cite: 1]. | Usabilidad |
| RNF-04 | El sistema debe garantizar la consistencia de los datos mediante transacciones seguras en la base de datos relacional para evitar pérdidas de información[cite: 1]. | Confiabilidad |

---

## 3. Modelo de casos de uso

**Diagrama de casos de uso:**

## 3. Modelo de casos de uso

**Diagrama de casos de uso del sistema:**

```mermaid
graph LR
    subgraph FarmaClick [Sistema FarmaClick]
        UC1((CU-01: Registrar Venta))
        UC2((CU-02: Gestionar Inventario))
        UC3((CU-03: Consultar Alertas de Stock/Vencimiento))
        UC4((CU-04: Generar Cierre de Caja))
    end

    Actor1[Encargado de Mostrador]
    Actor2[Administrador / Propietaria]

    Actor1 --> UC1
    Actor1 --> UC3
    Actor2 --> UC1
    Actor2 --> UC2
    Actor2 --> UC3
    Actor2 --> UC4 ```

**Especificación de casos de uso principales:**

### CU-01 · Registrar Venta

- **Actor(es):** Encargado de mostrador (Doris o personal)[cite: 1]
- **Precondición:** El sistema debe tener los medicamentos cargados en el inventario con stock disponible y precios actualizados[cite: 1].
- **Flujo principal:**[cite: 1]
  1. El usuario ingresa al módulo de Punto de Venta.
  2. El usuario busca el medicamento por nombre o principio activo.
  3. El sistema muestra los resultados coincidentes con su stock y precio.
  4. El usuario selecciona el producto e indica la cantidad deseada para agregarlo al carrito.
  5. El sistema recalcula el subtotal y el total general de la venta.
  6. El usuario ingresa el monto en efectivo entregado por el cliente y el sistema calcula el vuelto.
  7. El usuario confirma la venta.
  8. El sistema descuenta el stock de los productos vendidos y registra la transacción.
- **Flujos alternativos:**[cite: 1]
  - *Stock insuficiente:* Si la cantidad solicitada supera el stock actual, el sistema muestra una advertencia impidiendo agregar el producto hasta ajustar la cantidad.
- **Postcondición:** El inventario queda actualizado y la venta queda registrada para el arqueo diario[cite: 1].

### CU-02 · Gestionar Inventario

- **Actor(es):** Administrador / Señora Doris[cite: 1]
- **Precondición:** Ninguna[cite: 1].
- **Flujo principal:**[cite: 1]
  1. El usuario accede al módulo de inventario.
  2. Selecciona la opción de agregar un nuevo medicamento o editar uno existente.
  3. Completa o modifica los campos obligatorios (nombre, lote, precio, stock, fecha de vencimiento).
  4. El usuario guarda los cambios.
  5. El sistema valida los datos y actualiza la base de datos.
- **Flujos alternativos:**[cite: 1]
  - *Datos incompletos:* Si falta algún campo obligatorio, el sistema muestra un mensaje de error y solicita completarlo.
- **Postcondición:** Los cambios se reflejan inmediatamente en las consultas de mostrador y control de stock[cite: 1].

---

## 4. Modelo de dominio

**Diagrama de clases conceptual:**

`[Insertar imagen: diagramas/modelo-dominio.png]`[cite: 1]

El dominio del sistema se compone de las siguientes entidades principales[cite: 1]:
- **Medicamento:** Representa la información base del producto (nombre comercial, principio activo, forma farmacéutica y precio de venta).
- **Lote_Inventario:** Administra el control físico por cada partida de medicamentos, incluyendo su número de lote, stock actual, stock mínimo y fecha de vencimiento. Un medicamento puede tener múltiples lotes.
- **Venta:** Registra la transacción comercial realizada en el mostrador (fecha y hora, total pagado, monto recibido y vuelto).
- **Detalle_Venta:** Almacena los ítems específicos incluidos en una venta, vinculando la cantidad y precio unitario con el lote correspondiente.

---

## 5. Diagramas de comportamiento

**Diagrama de secuencia — Proceso de Venta:**

`[Insertar imagen: diagramas/secuencia-flujo-principal.png]`[cite: 1]

Este flujo representa la interacción donde el encargado selecciona los productos en la interfaz de **React (Front-end)**, el cual realiza una petición HTTP a la API de **Node.js (Back-end)** para consultar y actualizar la base de datos **PostgreSQL**, procesando el cálculo del vuelto y descontando el stock de forma segura[cite: 1].

---

## 6. Prototipo de interfaz (mockups)

**Pantalla — Punto de Venta (Mostrador):**

`[Insertar imagen: diagramas/mockup-pantalla1.png]`[cite: 1]

> *Descripción:* Interfaz optimizada para agilizar la atención en el mostrador mediante una barra de búsqueda rápida, visualización de lotes y stock disponible, y el cálculo automatizado del vuelto en efectivo[cite: 1].

**Pantalla — Alertas de Vencimiento y Stock Mínimo:**

`[Insertar imagen: diagramas/mockup-pantalla2.png]`[cite: 1]

> *Descripción:* Panel de control visual que advierte de forma anticipada sobre medicamentos con stock crítico o próximos a caducar para prevenir pérdidas económicas[cite: 1].

---

## 7. Reglas del negocio

| ID | Regla |
|---|---|
| RN-01 | Ningún medicamento cuyo lote se encuentre vencido podrá ser comercializado ni incluido en una venta activa dentro del sistema[cite: 1]. |
| RN-02 | El sistema no permitirá registrar una venta si la cantidad solicitada de un medicamento supera el stock físico disponible en el inventario[cite: 1]. |
| RN-03 | Las modificaciones de precios de venta sólo podrán ser realizadas por el rol de administración y se aplicarán de forma inmediata a las siguientes transacciones[cite: 1]. |

---

## 8. Matriz de trazabilidad

| Requisito | Caso(s) de uso relacionado(s) |
|---|---|
| RF-01 | CU-02 (Gestionar Inventario)[cite: 1] |
| RF-02 | CU-01 (Registrar Venta)[cite: 1] |
| RF-03 | CU-01 (Registrar Venta)[cite: 1] |
| RF-04 | CU-01 (Registrar Venta)[cite: 1] |
| RF-05 | Módulo de Alertas / Dashboard[cite: 1] |
| RF-06 | Módulo de Alertas / Reportes[cite: 1] |
| RF-07 | Módulo de Arqueo y Caja[cite: 1] |

---

[← Anterior: Conceptualización](conceptualizacion.md) · [Siguiente: Diseño →](diseno.md)
