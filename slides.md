---
theme: default
background: https://img.freepik.com/premium-photo/big-data-concept-digital-data-flow-transferring-big-data-transfer-storage-data-sets-database-protection-secure-transmission-information-blockchain-networks-3d-rendering_34629-1161.jpg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Presentacion Inteligencia de Negocios I
  Integrantes:
drawings:
  persist: false
transition: slide-left
title: OLAP y OLTP
layout: cover
---

# Diferencias entre <br> OLAP y OLTP

Integrantes: 

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<img
  class="absolute top-0 right-0 w-64 mt-2 mr-2 "
  src="/logoblanco.png"
/>

---
layout: intro
transition: slide-down
---

# Introduccion

## ¿Qué son OLAP y OLTP?
- **OLAP** (Procesamiento Analítico en Línea) y **OLTP** (Procesamiento de Transacciones en Línea) son dos tipos fundamentales de sistemas de procesamiento de datos en el mundo de las bases de datos.
- Ambos sistemas tienen diferentes objetivos y están diseñados para resolver diferentes problemas en el ámbito empresarial.

- Con el crecimiento exponencial de los datos, las empresas necesitan herramientas más eficientes para procesar y analizar la información.
- Mientras que OLTP se centra en la gestión de transacciones diarias (por ejemplo, ventas, compras, actualizaciones), OLAP se encarga del análisis y consulta de grandes cantidades de datos para ayudar en la toma de decisiones.

<img
  class="absolute top-0 right-0 w-42 mt-2 mr-2 "
  src="/logocolor.png"
/>

---
layout: default
transition: fade
---

## Importancia de OLAP y OLTP en las Empresas
- **OLAP**: 
  - Ayuda en la toma de decisiones al proporcionar vistas multidimensionales de los datos.
  - Facilita análisis profundos, como tendencias de ventas a lo largo del tiempo o comparaciones de rendimiento entre diferentes regiones.
  
- **OLTP**:
  - Garantiza que las transacciones diarias se procesen de manera eficiente y sin errores.
  - Es esencial para gestionar operaciones diarias, tales como control de inventario, gestión de nómina y mantenimiento de registros de clientes.

<img
  class="absolute top-0 right-0 w-42 mt-2 mr-2 "
  src="/logocolor.png"
/>

---
layout: image-left
image: /dbimage.jpg
---

# Definición y Propósito

# OLTP - Procesamiento de Transacciones en Línea

## Definición
- Sistema transaccional en línea para gestionar modificaciones en bases de datos.

## Funciones principales
- Insertar, actualizar, eliminar datos.
- Consultas simples y rápidas.
- Enfasis en modificar la base de datos más que en hacer consultas complejas.


<img
  class="absolute top-0 right-0 w-42 mt-2 mr-2 "
  src="/logocolor.png"
/>

---
layout: default
transition: slide-down
---

# Características de OLTP

## Uso Compartido
- Diariamente, muchos usuarios interactúan con el sistema.

## Base de Datos Normalizada 
- Se emplea generalmente la 3NF (Tercera Forma Normal) para evitar redundancia y mejorar la integridad de datos.
  
## Necesidad de Respaldo
- Errores pueden comprometer la integridad de la base de datos.
- Continuamente se realizan respaldos para garantizar integridad.

<img
  class="absolute top-0 right-0 w-64 mt-2 mr-2 "
  src="/logocolor.png"
/>

---
layout: image-right
---

# OLAP - Procesamiento Analítico en Línea

## Definición
- Sistema de procesamiento analítico diseñado para realizar grandes consultas a bases de datos.

## Diferencias clave con OLTP
- No necesita bases de datos normalizadas.
- Foco en consultas, no en modificaciones.

<img
  class="absolute top-0 right-0 w-64 mt-2 mr-2 "
  src="/logocolor.png"
/>

<div class="text-right flex">
  <img src="/olapcube.png" alt="Description of Image" class="absolute left-125 top-50 h-70 border rounded shadow">  
</div>




---
layout: default
transition: slide-down
---

# Características de OLAP

## Frecuencia de Consultas
- Se hacen de forma esporádica: desde 1 a 5 años, según el usuario.

## Duración de las Consultas
- Las consultas suelen ser más prolongadas que las transacciones en OLTP.

## Almacenamiento de datos históricos
- Para ofrecer tendencias y análisis de comportamiento a lo largo del tiempo.

<div style="text-align: right;">
  <img src="/olapcube.png" alt="Description of Image" style="float: right; width: 37%; margin-left: 1em; margin-bottom: 1em;">
</div>

<img
  class="absolute top-0 right-0 w-42 mt-2 mr-2 "
  src="/Logo_VG_blanco.png"
/>


---
layout: image-right
transition: fade
image: /path-to-data-architecture-image.jpg
---

# Arquitectura de Datos

## Bases de Datos OLAP
- Prioriza la lectura de datos sobre operaciones de escritura.
- Rápida y eficiente en consultas complejas en grandes volúmenes de datos.
- Disponibilidad es de baja prioridad.
- Principal caso de uso: análisis.

## Bases de Datos OLTP
- Prioriza operaciones de escritura de datos.
- Optimizada para cargas de trabajo con muchas escrituras.
- Actualiza datos transaccionales de alta frecuencia sin comprometer integridad.

---
layout: default
transition: slide-up
---

# Arquitectura de Datos

# Estructura de Datos

## OLTP: Procesamiento de Transacciones
- Bases de datos orientadas a procesamiento de transacciones.
- Acceso optimizado para lecturas y escrituras frecuentes.
- Estructura de datos según el nivel de aplicación.
- Formatos de datos pueden variar entre departamentos.
- Historial de datos limitado a lo actual o reciente.

## OLAP: Procesamiento Analítico
- Bases de datos orientadas al análisis.
- Acceso generalmente de solo lectura.
- Estructura de datos según áreas de negocio.
- Historial a largo plazo, típicamente de 2 a 5 años.


---
layout: default
transition: slide-down
---

# Tipos de Consultas

## Tipos de Consultas en OLAP

- Consulta de corte (Slice): Selecciona una sola dimensión y una posición en esa dimensión para obtener una "rebanada" de los datos multidimensionales.
- Consulta de poda (Dice): Selecciona un subconjunto de datos al especificar posiciones en múltiples dimensiones.
- Consulta de perforación (Drill-Down): Amplía la información al moverse desde un nivel de resumen a un nivel de detalle más bajo.
- Consulta de resumen (Roll-Up): Reduce la información al moverse desde un nivel de detalle a un nivel de resumen más alto.
- Consulta de rotación (Pivot): Cambia las dimensiones en los ejes para proporcionar diferentes perspectivas de los datos.
- Consulta de tendencias (Time Series): Analiza cómo una medida ha evolucionado a lo largo del tiempo.
- Consulta de comparación: Compara el rendimiento entre diferentes dimensione.
- Consulta de porcentaje (Percentage): Calcula el porcentaje de una medida con respecto a otra.

---
layout: image-right
transition: fade
image: /path-to-application-example-image.jpg
---
# Tipos de Consultas

## Tipos de Consultas en OLTP
- CRUD (Crear, Leer, Actualizar, Eliminar): Operaciones básicas en registros de bases de datos.
- Transacciones que involucran múltiples operaciones CRUD asegurando la integridad de la base de datos.
- Consulta de inserción: Agregar nuevos registros a la base de datos.
- Consulta de actualización: Modificar los valores de uno o más campos en un registro existente.
- Consulta de eliminación: Eliminar registros de la base de datos.
- Consulta de unión: Combinar información de múltiples tablas para obtener un conjunto de resultados más completo.obtener detalles de pedidos junto con los datos del cliente
- Consulta de agrupamiento: Realizar operaciones de agregación en los datos, como calcular sumas, promedios, máximos o mínimos en grupos de registros.
- Consulta de ordenamiento: Ordenar los resultados de una consulta en función de uno o más campos.
- Consulta de existencia: Verificar si un registro o valor existe en la base de datos.




---
layout: image-right
transition: zoom-in
image: /path-to-oltp-application-image.jpg
---

# Ejemplos de Aplicación

## Ejemplos de Uso de OLAP
- Análisis de Ventas y Comportamiento del Cliente.
- Planificación Financiera y Presupuestaria.
- Gestión de Inventarios y Suministros.
- Segmentación de Clientes y Personalización.
- Análisis de Redes Sociales y Opiniones de los Clientes.

<img
  class="absolute top-0 right-0 w-100 mt-35 mr-4 "
  src="/ventas.png"
/>

---
layout: default
transition: slide-up
---
# Ejemplos de Aplicación

## Ejemplos de Uso de OLTP

- Sistema de Gestión de Pedidos en Comercio Electrónico.
- Sistema Bancario y Cajeros Automáticos.
- Sistema de Reservas en la Industria Hotelera.

<img
  class="absolute top-0 right-0 w-100 mt-35 mr-4 "
  src="/ejemplooltp.png"
/>

---
layout: image-right
transition: slide-down
image: https://www.ceupe.com/images/easyblog_articles/2754/beneficio-empresarial.jpg
---

# Beneficios de las Empresas al Utilizar OLAP
- Mejor toma de decisiones basada en insights profundos.
---
layout: default
---
# Beneficios de las Empresas al Utilizar OLTP
- Procesamiento eficiente de transacciones diarias.
- Asegurar la integridad y consistencia de los datos en operaciones diarias.

---
layout: default
transition: zoom-in
---

# Consideraciones de Diseño

## Factores Generales a Considerar

- **Objetivos de la empresa:** Esenciales para definir la dirección del diseño.
- **Tipo de datos:** OLAP usa datos multidimensionales, mientras OLTP usa datos relacionales.
- **Volumen de datos:** OLAP maneja grandes volúmenes para análisis profundo.
- **Requisitos de rendimiento:** Especialmente relevante para OLAP con consultas complejas.

---
layout: image-right
transition: slide-up
image: /path-to-oltp-design-consideration-image.jpg
---

# Consideraciones de Diseño

## Consideraciones para sistemas OLAP

- **Modelo de datos:** Uso predominante de modelos de datos multidimensionales como cubos OLAP.
- **Limpieza de datos:** Importante garantizar datos limpios y ordenados.
- **Herramientas de análisis:** Seleccionar herramientas acorde al tipo de análisis requerido.

---
layout: image-left
transition: fade
image: /path-to-optimization-image.jpg
---

# Consideraciones de Diseño

## Consideraciones para sistemas OLTP

- **Modelo de datos:** Generalmente basados en modelos de datos relacionales.
- **Estructura de datos:** Organización eficiente para acceso rápido.
- **Procedimientos de transacción:** Garantizar la integridad de los datos es fundamental.

---
layout: image-right
image: https://www.pngmart.com/files/7/Optimization-Transparent-Images-PNG.png
---

# Consideraciones de Diseño

# Optimización y rendimiento
- **Uso de hardware adecuado:** Vital para satisfacer las demandas del sistema.
- **Optimización de consultas:** Mejora la velocidad y eficiencia del sistema.
- **Caché de datos:** Almacena datos frecuentes para un acceso más rápido.
- **Diseño de índices:** Facilita consultas de búsqueda más rápidas.

---
layout: default
---

# Gracias por su atención

