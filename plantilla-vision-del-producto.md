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
Un sistema para ayudar a un hotel pequeño llevar un mejor control de los productos y artículos que tiene disponibles. Permite saber qué bebidas y alimentos hay en los minibares de cada habitación, así como controlar otros artículos utilizados en el hotel, como toallas, cobijas, sábanas y almohadas. El sistema permite registrar cuándo un artículo es utilizado, retirado o repuesto, para conocer en todo momento qué hay disponible, qué se encuentra en cada habitación y qué artículos necesitan ser reemplazados o comprados.

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

### Dentro del alcance
El sistema incluirá el control de las 12 habitaciones del hotel, el inventario de productos de los minibares y de blancos como sábanas, toallas, cobijas y almohadas. Permitirá registrar los productos colocados en las habitaciones, los consumos realizados, las reposiciones, las entradas y salidas del inventario y el estado de los artículos. También permitirá consultar qué productos se encuentran disponibles, cuáles necesitan reposición y qué artículos se encuentran en cada habitación. El sistema contará con usuarios para recepción, personal de limpieza y dueño del hotel, además de un historial de los movimientos realizados.

### Explícitamente fuera del alcance
El sistema no incluirá reservaciones de habitaciones, cobro del hospedaje, control de nómina, facturación electrónica, ni realización de pedidos o pagos a proveedores. Tampoco tendrá una aplicación destinada a los huéspedes. 

**Por qué queda fuera:**

Estas funciones quedan fuera porque no forman parte del problema principal que se busca resolver y agregar algunas de ellas aumentaría considerablemente el tamaño y complejidad del proyecto para el tiempo disponible durante el semestre.

## 4. Tipo de sistema y restricciones

**Tipo de sistema:**
Sistema de información

**Por qué es de ese tipo:**
El Hotel Innventario es un sistema de información porque permite registrar, consultar, actualizar y compartir información relacionada con los productos y artículos del hotel. Su función principal es ayudar al personal de recepción, al personal de limpieza y al dueño del hotel a conocer el estado de los productos en las habitaciones y del inventario general, para facilitar las tareas de registro, reposición y toma de decisiones.
**Atributos de calidad que impone:**
| Atributo | Por qué importa en mi caso | Qué pasa si no se cumple |
|---|---|---|
| **Exactitud** | La información del inventario debe coincidir con los productos que realmente se encuentran en las habitaciones y en el almacén. | Se pueden cobrar consumos incorrectamente, comprar productos innecesarios o quedarse sin productos importantes. |
| **Disponibilidad** | El personal de recepción y limpieza necesita consultar y registrar información cuando está realizando sus actividades en las habitaciones. | El personal tendría que volver a utilizar registros en papel o esperar para poder actualizar la información. |
| **Seguridad** | No todos los usuarios necesitan modificar la misma información. Por ejemplo, el dueño puede consultar el inventario general, mientras que recepción y limpieza realizan registros relacionados con sus actividades. | Un usuario podría modificar información que no le corresponde y provocar errores o pérdida de información. |

**Reglas de negocio que ya identifiqué:**

1. Control de merma y baja definitiva de blancos: Ningún artículo de blancos puede eliminarse del inventario global sin haber pasado previamente por el estado "En lavandería" o "Dañado", y la baja por merma o extravío únicamente puede ser autorizada por el perfil del Dueño.
2. Auditoría automática de cargos al Check-Out: Todo producto de minibar registrado como faltante durante la inspección de salida genera de forma automática una alerta de cargo en la cuenta del huésped en recepción antes de permitir el cierre del check-out.
3. Bloqueo de asignación por dotación incompleta: Una habitación no puede marcarse en estado "Disponible / Lista para entrega" si su inventario físico validado por el personal de limpieza no cubre el 100% de la dotación estándar asignada de blancos (por ejemplo: 2 almohadas, 1 juego de sábanas y 2 toallas).

---

## 5. Ciclo de vida elegido

**Modelo elegido: Ágil**

**Por qué le conviene a este proyecto:**

El modelo ágil le conviene a Hotel Innventario porque, aunque el problema que se busca resolver está definido, algunos requisitos pueden cambiar o surgir nuevos conforme se conozcan mejor las necesidades del personal de recepción, limpieza y del dueño del hotel. El cliente y los usuarios pueden proporcionar retroalimentación durante el desarrollo, lo que permite realizar ajustes conforme avance el proyecto. El nivel de riesgo técnico es bajo, ya que se trata de un sistema de información para un hotel pequeño de 12 habitaciones.

### Alternativas descartadas

**Alternativa 1: Cascada**

Se descartó el modelo en cascada porque requiere definir y establecer los requisitos con mayor precisión desde el inicio del proyecto. En Hotel Innventario algunos requisitos pueden cambiar conforme se reciba retroalimentación de los usuarios y se conozca mejor el funcionamiento del hotel. Esto haría más difícil realizar cambios en etapas posteriores del desarrollo.

**Alternativa 2: Espiral**

Se descartó el modelo espiral porque está orientado principalmente a proyectos grandes o con un nivel de riesgo técnico elevado, donde es necesario analizar y reducir riesgos de manera constante. Hotel Innventario es un sistema de información para un hotel pequeño de 12 habitaciones y no presenta riesgos técnicos o de seguridad que justifiquen la complejidad de este modelo.

---
