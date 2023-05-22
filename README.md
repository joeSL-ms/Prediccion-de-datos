# CRO con AB Testing

<p align="center">
  <img src="https://github.com/Anton-Utray/CRO/blob/main/IMG/Portada-CRO.jpg" alt="Portada" width="500">
</p>


1. [Objetivo](#objetivo)
2. [Prototipo](#prototipo)
3. [Analisis y Conclusiones](#analisis)



## Objetivo

Proyecto en colaboración con el bootcamp UX/UI donde el objetivo es optimizar la tasa de conversión de un ecommerce a través de una versión control (original) y una de testeo, con cambios, para analizar y comparar el rendimento entre ambas versiones gracias a AB Testing.

<details>
<summary>Flujo de trabajo</summary>
<br>

 - UX/UI presenta el prototipo de su pagina web al equipo de data. En nuestro caso se trata de una pagina web de venta de libros Altamerea. 
 - Data salimos a recopilar datos de uso, preguntando a voluntarios de probar el prototipo. 
    - Se pregunta a los voluntarios: 
        - Buscar los libros de la categoria femenina
        - Dentro de la categoria femenina encontrar los que corresponden a tapa dura
        - Encontrar el libro de Michelle Obama y completar el checkout. 
    - Nos encargamos de medir: el tiempo en realizar diversas acciones.
    - Clicks totales vs clicks utiles.
    - Comentarios de tipo general que nos den *feedback* general.
- Reunion entre ambos equipos para retroalimentar y decidir sobre los cambios a efectuar para la versión control. 
- Segunda recopilación de datos de campo. 
- Alimentación de datos al sistema para medir y cuantificar las mejoras. 

</details>

<details>
<summary>KPIs</summary>
<br>

El objetivo es optimizar la tasa de clicks utiles vs clicks totales en el proceso de compra. 

De igual manera tenemos como objetivo reducir la media de tiempo para finalizar la compra. 

Para tal efecto, definimos los siguientes KPIs como objetivo:

 - Tasa de clicks optima para realizar compra: 12
 - Tiempo para realizar checkout: 1 minuto. 

 Estos KPIS luego nos van a servir a la hora de categorizar los resultados (True/False) para efectuar un modelo bayesiano. 

</details>

## Prototipo

<p align="center">
  <img src="https://github.com/Anton-Utray/CRO/blob/main/IMG/cambios%20web.png" alt="Cambios" width="800">
</p>

Para poder reducir el numero de clicks y reducir el tiempo dedicado al proceso de compra, se realizaron las siguientes adecuaciones al prototipo:

  - Filtro desplegaod por *default* para que el usuario pueda visualizar directamente las opciones.
  - Opción de 'pagar ya' incluida en los *thumbnail* de los productos del landing page. (Antes el usuario tenia que ingresar al Product Page).
  - El esquema de color favoriza visualmente al botón de 'pagar ya'. Anteriormente estaba destacada la opción de 'agregar a cesta' y añadía un click adicional.


## Analisis y Conclusiones

A continuación se presentan los resultados de ambos trabajos de campo:

- En la primera muestra el minimo de clicks es de 13, pero por ciertos metodos de construccion tendia a 18 y el tiempo promedio era de 1:30.
- En la segunda pagina el minimo de clicks es de 10, y este en la reconstruccion tiende hasta 14 y el tiempo promedio es de 50 seg. 

</div>
<div align="center">
  Dispersión de valores de clicks y tiempo para ambas muestras
  
  ![image](https://github.com/joeSL-ms/proye/assets/127346073/590e48b6-dd3b-41df-91ee-e3502f26c00b)
  
  Medias de cada muestra
  
  ![image](https://github.com/joeSL-ms/proye/assets/127346073/cded53a4-8422-4531-aa3e-045fce8bffe9)
</div>
<div>

  Los graficos de arriba nos muestran claramente las mejoras entre los prototipos. Sin embargo, para asegurar una mayor fiabilidad en los resultados, realizamos un modelo bayesiano para comprobar nuestra hipothesis. 

Esta se calcula en función de las tasas de exito de los dos parametros. Es decir, el numero de personas que completan el proceso de compra en 12 clicks o menos y en 1 minuto o menos. 

| Clicks | Tiempo |
| --------- | --------- |
| Caso 1 | Caso 2 |
|Se observa una mejora del 400% en la tasa de clicks con probabilidad del 99,90% | Se observa una mejora en la tasa de tiempo de 116,67%  con una probabilidad del 99.43%.  |
| <div align="center" colspan="2"> ![image](https://github.com/joeSL-ms/proye/assets/127346073/af1933f5-c203-4873-a0b0-5c83badce8a2)</div> | <div align="center"> ![image](https://github.com/joeSL-ms/proye/assets/127346073/284b07c1-bbac-47ee-854a-09749ab21411)</div> |
  </div>
