# Sprint5
# 🎬 Proyecto de Analítica de Datos con MongoDB

Este repositorio contiene la resolución del caso práctico de análisis de datos NoSQL para una plataforma de entretenimiento cinematográfico. El proyecto demuestra la capacidad analítica para explorar, filtrar, agregar y procesar información en MongoDB atendiendo a los requerimientos del cliente.

> 📄 **Nota:** Las consultas detalladas de cada ejercicio y sus correspondientes capturas de pantalla de ejecución se encuentran documentadas en el archivo **`Sprint5`**.

---

## 📌 Descripción del Proyecto

El objetivo principal de este trabajo es evaluar y aplicar técnicas de consulta sobre bases de datos NoSQL para resolver problemas analíticos reales. Se trabaja sobre colecciones interrelacionadas que simulan el entorno de producción de un servicio de streaming y catálogo cinematográfico.

---

## 🗃️ Estructura de la Base de Datos

La base de datos se compone de 5 colecciones principales:

* **`users`**: Información de usuarios/as registrados (nombres, emails y contraseñas cifradas).
* **`theaters`**: Datos de cines y salas de proyección (ID, dirección física y ubicación geoespacial en formato GeoJSON).
* **`sessions`**: Registro de sesiones de usuario activas y tokens de autenticación JWT.
* **`movies`**: Catálogo de películas con metadatos completos (trama, géneros, duración, elenco, directores, premios, clasificaciones y notas de IMDb/Rotten Tomatoes).
* **`comments`**: Reseñas y comentarios publicados por los usuarios sobre las películas (autor, ID de película, texto y fecha).

---

## 📋 Resumen de Ejercicios Realizados

El análisis se estructuró en tres niveles de complejidad incremental:

### 🟢 Nivel 1: Exploración y Filtrado Básico
* **Ejercicio 1:** Consultas exploratorias de conteo y ordenación en `comments`, `users`, `theaters` y `movies` (primeros registros, totales y filtros simples por estado/género).
* **Ejercicio 2:** Filtrado condicional combinado con operadores lógicos (`$or`) sobre películas de 1932 por género o idioma.
* **Ejercicio 3:** Consultas de rango de fechas y valores numéricos en arrays/objetos anidados (películas de EE. UU. producidas entre 2012 y 2014 con rango de premios ganados).

### 🟡 Nivel 2: Agregaciones y Agrupaciones
* **Ejercicio 1:** Búsqueda y conteo de comentarios mediante expresiones regulares (`$regex`) para filtrar por dominios de correo específicos (`@gameofthron.es`).
* **Ejercicio 2:** Uso de *Aggregation Framework* (`$match`, `$group`, `$sort`) para contabilizar la densidad de cines por código postal en el estado de Washington DC (`DC`).

### 🔴 Nivel 3: Proyecciones Avanzadas y Datos Geoespaciales
* **Ejercicio 1:** Filtrado por director y rango de puntuación en IMDb (`$gte`, `$lte`), aplicando proyecciones (`$project`) para formatear la salida limpiando campos no relevantes (como métricas de *Rotten Tomatoes*).
* **Ejercicio 2:** Análisis y representación geoespacial de la colección `theaters` utilizando las coordenadas GeoJSON (`location.geo`) para su visualización interactiva en mapas mediante MongoDB Compass y herramientas GIS.

---

## 🎯 Objetivos Alcanzados

- [x] Creación e importación exitosa de las colecciones en MongoDB.
- [x] Construcción de consultas eficientes en MongoDB Shell (`mongosh`) y MongoDB Compass.
- [x] Aplicación de Pipelines de Agregación para agrupación y análisis estadístico.
- [x] Procesamiento y representación de datos geográficos GeoJSON.

---

## 🛠️ Tecnologías Utilizadas

* **Motor de Base de Datos:** MongoDB
* **Gestión y Herramientas GUI:** MongoDB Compass, `mongosh` (MongoDB Shell)
* **Estándar Geográfico:** GeoJSON / Leaflet
