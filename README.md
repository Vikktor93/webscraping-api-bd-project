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

En la página inicial: 
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