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

<!-- Top-right corner logo -->

<img
  class="absolute top-0 right-0 w-64 mt-4 mr-4 "
  src="/Logo_VG_blanco.png"
/>



<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
layout: intro
---



# Introduccion


## ¿Qué son OLAP y OLTP?
- **OLAP** (Procesamiento Analítico en Línea) y **OLTP** (Procesamiento de Transacciones en Línea) son dos tipos fundamentales de sistemas de procesamiento de datos en el mundo de las bases de datos.
- Ambos sistemas tienen diferentes objetivos y están diseñados para resolver diferentes problemas en el ámbito empresarial.

- Con el crecimiento exponencial de los datos, las empresas necesitan herramientas más eficientes para procesar y analizar la información.
- Mientras que OLTP se centra en la gestión de transacciones diarias (por ejemplo, ventas, compras, actualizaciones), OLAP se encarga del análisis y consulta de grandes cantidades de datos para ayudar en la toma de decisiones.


<img
  class="absolute top-0 right-0 w-42 mt-4 mr-4 "
  src="/Logo_VG_blanco.png"
/>

---
layout: intro
---

## Importancia de OLAP y OLTP en las Empresas
- **OLAP**: 
  - Ayuda en la toma de decisiones al proporcionar vistas multidimensionales de los datos.
  - Facilita análisis profundos, como tendencias de ventas a lo largo del tiempo o comparaciones de rendimiento entre diferentes regiones.
  
- **OLTP**:
  - Garantiza que las transacciones diarias se procesen de manera eficiente y sin errores.
  - Es esencial para operaciones diarias como inventario, nómina y registros de clientes.




<img
  class="absolute top-0 right-0 w-42 mt-4 mr-4 "
  src="/Logo_VG_blanco.png"
/>

---
layout: default
---

# Table de contenido


<Toc columns:2 />
<img
  class="absolute top-0 right-0 w-42 mt-4 mr-4 "
  src="/Logo_VG_blanco.png"
/>

---
transition: slide-up

level: 2
---

# Definición y Propósito

## OLAP - Procesamiento Analítico en Línea
- Definición: Sistema diseñado para analizar y consultar grandes volúmenes de datos en múltiples dimensiones.
- Propósito: Facilitar la toma de decisiones mediante la identificación de tendencias, patrones y anomalías en los datos.

## OLTP - Procesamiento de Transacciones en Línea
- Definición: Sistema diseñado para manejar grandes cantidades de transacciones cortas (como consultas o actualizaciones).
- Propósito: Mantener la integridad de la base de datos en un ambiente multiusuario y asegurar la eficiencia de las operaciones diarias de negocio.

<img
  class="absolute top-0 right-0 w-42 mt-4 mr-4 "
  src="/Logo_VG_blanco.png"
/>

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Arquitectura y Estructura de Datos

## Arquitectura de Datos
- Descripción de cómo los sistemas OLAP y OLTP están estructurados a nivel de hardware y software.
- Consideraciones sobre la distribución, redundancia y escalabilidad.




---
layout: image-right
---
# Arquitectura y Estructura de Datos
## Estructura de Datos
- OLAP: Uso común de cubos de datos que permiten consultas multidimensionales.
- OLTP: Uso de bases de datos relacionales con esquemas normalizados para eficiencia en transacciones.
---
layout: image-right
---

# Tipos de Consultas

## Tipos de Consultas en OLAP
- Drill-down y Drill-up: Moverse entre diferentes niveles de granularidad.
- Slice-and-dice: Visualizar datos desde diferentes perspectivas.
- Roll-up: Agregar datos en una dimensión específica.



---
layout: image-right
---
# Tipos de Consultas

## Tipos de Consultas en OLTP
- CRUD (Crear, Leer, Actualizar, Eliminar): Operaciones básicas en registros de bases de datos.
- Transacciones que involucran múltiples operaciones CRUD asegurando la integridad de la base de datos.



---
class: px-20
---
# Ejemplos de Aplicación

## Ejemplos de Uso de OLAP
- Análisis de ventas por región y categoría de producto a lo largo del tiempo.
- Comparación de rendimiento de campañas de marketing en diferentes canales.


---
layout: image-right
---
# Ejemplos de Aplicación


## Ejemplos de Uso de OLTP
- Registro de una venta en un sistema de punto de venta.
- Actualización de la dirección de un cliente en un sistema CRM.



---
preload: false
---

# Beneficios de las Empresas al Utilizar OLAP
- Mejor toma de decisiones basada en insights profundos.
- Flexibilidad para adaptarse a cambiantes requerimientos de análisis.

---
# Beneficios de las Empresas al Utilizar OLTP
- Procesamiento eficiente de transacciones diarias.
- Asegurar la integridad y consistencia de los datos en operaciones diarias.


---

# Consideraciones de Diseño

## Consideraciones de diseño para sistemas OLAP
- Garantizar capacidad de respuesta en consultas complejas.
- Diseño de cubos de datos eficientes y estructuras relacionadas.

## Consideraciones de diseño para sistemas OLTP
- Optimización para transacciones cortas.
- Asegurar robustez y recuperabilidad ante fallos.


---
layout: image-right
---
# Optimización y rendimiento
- Técnicas para mejorar el rendimiento, como indexación, caché y distribución.
- Desafíos comunes y soluciones en la optimización de OLAP y OLTP.


---
layout: center
class: text-center
---

# Linkografía y Bibliografía
- Lista de fuentes consultadas y recomendaciones para lectura adicional.