# Visión del producto

> **Plantilla del curso · Ingeniería de Software I · SIS3407**

---

**Autor:** Jose Fernando Saucedo Balderas  
**Fecha de la última versión:** 15/08/2026  
**Repositorio:** Anáhuac  

---

## 1. Descripción del sistema

**Nombre del sistema:** Hotel Innventario

**Descripción:**
Un sistema para ayudar al hotel Agua Santa a llevar un mejor control de los productos y artículos que tiene disponibles. Permite saber qué bebidas y alimentos hay en los minibares de cada habitación, así como controlar otros artículos utilizados en el hotel, como toallas, cobijas, sábanas y almohadas. El sistema permite registrar cuándo un artículo es utilizado, retirado o repuesto, para conocer en todo momento qué hay disponible, qué se encuentra en cada habitación y qué artículos necesitan ser reemplazados o comprados.

---

## 2. Problema y usuarios


**El problema:** 
El hotel tiene dificultades para llevar un control preciso de los productos y artículos que tiene disponibles, los que se encuentran en cada habitación y los que necesitan ser repuestos. Esto puede provocar pérdidas, compras innecesarias, falta de productos y problemas de comunicación entre los empleados. 

**Cómo se resuelve hoy sin el sistema:**
Actualmente, el control de los artículos que se encuentran en las habitaciones del hotel se realiza de manera manual mediante una hoja de registro. Esta hoja contiene por un lado el inventario de blancos de cada habitación, como sábanas, cobijas, almohadas, toallas y demás ropa de cama, mientras que por el otro lado se registra el contenido del minibar, incluyendo bebidas y alimentos. El personal de limpieza es el encargado de revisar los artículos de cada habitación y llenar la hoja de forma manual. 
**Usuarios del sistema:**

| Tipo de usuario | Qué necesita del sistema | Qué le preocupa |
|---|---|---|
| Personal de recepción | Consultar y registrar los productos que se colocan en los minibares de cada habitación, así como consultar los consumos registrados para poder cobrarlos al huésped durante el check-out. | Cobrar correctamente los consumos y contar con información confiable sobre los productos que deben reponerse. |
| Personal de limpieza | Consultar los artículos que debería tener cada habitación y registrar lo que encuentra durante la revisión, incluyendo los productos del minibar y los blancos. | Que la información registrada coincida con lo que realmente hay en la habitación y detectar correctamente productos consumidos o artículos faltantes. |
| Dueño del hotel | Consultar el inventario general del hotel, las existencias de productos y artículos, los consumos y los elementos que necesitan reposición. | Contar con información actualizada y confiable para saber qué productos necesita comprar y evitar quedarse sin artículos necesarios. |

**Un conflicto entre usuarios:**

El dueño del hotel necesita conocer con precisión cuántos blancos hay disponibles y dónde se encuentran para poder tomar decisiones de compra. Sin embargo, el personal de limpieza necesita poder indicar cuando un artículo no se encuentra temporalmente en una habitación porque está en lavandería, está dañado, se encuentra pendiente de reposición o por alguna otra situación. Por lo tanto, el sistema deberá permitir diferentes estados para los artículos, de manera que el dueño pueda conocer la situación real del inventario sin dificultar el trabajo del personal de limpieza.

---

## 3. Alcance

*Instrucción: lo que escribes en "fuera del alcance" es lo que después evita que el proyecto crezca sin control. Sé específico: "reportes" no dice nada, "reportes de ventas mensuales exportables a PDF" sí.*

### Dentro del alcance

-
-
-
-

### Explícitamente fuera del alcance

-
-
-

**Por qué queda fuera:**

*Instrucción: para al menos una de las exclusiones, explica la razón. Puede ser tiempo, complejidad, o que no aporta al problema central.*

---

## 4. Tipo de sistema y restricciones

*Instrucción: identifica de qué tipo es tu sistema y qué te obliga a garantizar ese tipo. Un sistema de información y un sistema crítico no se diseñan igual.*

**Tipo de sistema:**

*(De información · Embebido · Crítico · Web y SaaS · De datos y análisis)*

**Por qué es de ese tipo:**

**Atributos de calidad que impone:**

| Atributo | Por qué importa en mi caso | Qué pasa si no se cumple |
|---|---|---|
| | | |
| | | |
| | | |

**Reglas de negocio que ya identifiqué:**

*Instrucción: reglas que no son obvias desde fuera y que alguien que conoce el dominio tendría que explicarte. Si no encuentras ninguna, tu caso puede ser demasiado simple.*

1.
2.
3.

---

## 5. Ciclo de vida elegido

*Instrucción: este apartado se trabaja en la semana 3, después de ver los modelos de desarrollo. La justificación pesa más que la elección: no hay un modelo correcto, hay uno defendible para tu caso.*

**Modelo elegido:**

**Por qué le conviene a este proyecto:**

*Instrucción: argumenta con las características reales de tu caso. Estabilidad de los requisitos, disponibilidad del cliente, nivel de riesgo, tamaño del equipo, frecuencia de entregas esperada.*

### Alternativas descartadas

**Alternativa 1:**

*Por qué la descarté:*

**Alternativa 2:**

*Por qué la descarté:*

---

## Antes de entregar

Reviso que el documento cumpla lo siguiente:

- [ ] La descripción del apartado 1 se entiende sin ser del área
- [ ] Hay al menos dos tipos de usuario con necesidades distintas
- [ ] Identifiqué un conflicto real entre usuarios
- [ ] El alcance dice qué queda fuera, no solo qué queda dentro
- [ ] Las exclusiones son específicas, no genéricas
- [ ] Identifiqué el tipo de sistema y al menos dos atributos de calidad
- [ ] Anoté al menos tres reglas de negocio no obvias
- [ ] Justifiqué el ciclo de vida contra dos alternativas descartadas
- [ ] El documento está en mi repositorio y se puede leer desde el navegador
- [ ] Borré todas las instrucciones en cursiva de la plantilla
