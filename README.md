<p align="left">
   <img src="https://img.shields.io/badge/Status-En%20Desarrollo-green?style=plastic">
   <img src="https://img.shields.io/badge/Python-3776AB?style=plastic&logo=python&logoColor=white"/>
   <img src="https://img.shields.io/badge/Jupyter-%23e58f1a.svg?style=plastic&logo=Jupyter&logoColor=white"/>

<img src="./assets/banner-scrapping.png"/>

## Proyecto Final - Web Scraping - Base de Datos - APIs

Este proyecto consiste en aplicar lo aprendido de Web Scraping, Base de Datos y APIs. Para esto, se desarrolló un producto de consulta de inmuebles con sus comercios cercanos. 

## Descripción 

### **PARTE 1** 

Usando Selenium, se solicita interactuar con la página web [Portal Inmobiliario](https://www.portalinmobiliario.com/) para seleccionar las opciones de búsqueda de inmuebles, según los valores de las variables definidas. Se solicita utilizar diferentes tipos de selectores para encontrar elementos y hacer clics o introducir texto. 

- En la página inicial: 
    - Filtrar según botón de tipo contrato.
    - Filtrar según botón de tipo inmueble.
    - Filtrar según botón de comuna de búsqueda.
    - Elegir la primera sugerencia de búsqueda.
    - Hacer clic en botón BUSCAR.


En la página de resultados: 
    - Filtrar por monto mínimo y máximo.
    - Recorrer la cantidad de páginas realizando lo siguiente: 
        - Extraer el título.
        - Extraer la unidad monetaria ($ o UF).
        - Extraer el precio.
        - Extraer el link del anuncio.
        - Crear un dataframe con estos resultados. 

- Para cada inmueble, se debe navegar a su enlace específico y extraer información adicional como la dirección completa. Luego se debe añadir esta información al dataframe existente.
- Usando Selenium, interactuar con la página web [Valor UF](https://valoruf.cl/) y obtener el valor de la UF al día de hoy (hoy = momento en que se ejecuta el código).
- Luego, se debe convertir los valores monetarios de los inmuebles desde UF a pesos chilenos.
- Proponer e implementar una forma para lidiar con las direcciones que tienen rango en su numeración, por ejemplo: “Avenida Manquehue 1200 – 1800, Las Condes”. Ya que esta es una forma que usan los dueños del inmueble para enmascarar la dirección real, pero necesitamos obtener un solo número para que funcione correctamente la API Geocoding.

### **PARTE 2** 

- Utilizando Geocoding API de Google obtener; latitud, longitud y place_id EXACTOS de cada dirección normalizada.
- Actualizar el dataframe existente con estas nuevas columnas.
- Utilizando Places API de Google obtener, para cada dirección, los lugares cercanos según el radio y rubros definidos.
- Crear un nuevo dataframe con esta información.

### **PARTE 3** 
- Utilizando la librería sqlite, crear una base de datos, definir su esquema y relaciones entre tablas. Posteriormente se debe guardar los 2 dataframes creados (el de inmuebles y el de lugares cercanos) en esta Base de Datos.
- Realizar consultas SQL para responder las siguientes preguntas:
    - ¿Cuál es el valor promedio de los 20 arriendos de dpto más baratos de “x comuna”?
    - ¿Cuál es la mediana de comentarios (user_ratinngs_total), de aquellos lugares cercanos, que tienen una valoración igual o superior a 4 estrellas y que corresponden a los 15 departamentos más baratos de “x comuna”?