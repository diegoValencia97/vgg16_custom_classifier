# Actividad integradora 3
-----------------------------
Diego Fernando Valencia Martínez
A01336815

-----------------------------
## ¿Qué hace el proyecto?

Se diseña un clasificador de imágenes que aprovecha la arquitectura VGG16 para reemplazar la última capa por una Softmax con 5 nodos que represente las nuevas a clasificar i.e. mono, león, hormiga, tortuga, búho. Por lo tanto, el entrenamiento ocurrió en las últimas dos capas de modo que se aprovecharan los pesos de las capas restantes previamente capaces de clasificar dentro de 1000 clases diferentes. El dataset de las 5 nuevas clases se obtuvo mediante un web scraper utilizando Selenium que explorara las bases de ImageNet y Shutterstock.  

-----------------------------        
## ¿Cuál es la importancia del proyecto?

Este proyecto representa sirve para demostrar la utilidad de "transfer learning" en lugar de diseñar una red neuronal desde cero. Apoyándose del estado del arte y los recursos open source pueden lograrse excelentes resultados, ahorrando tiempo y recursos. 

-----------------------------    
## Funcionamiento

El cuaderno de Jupyter permite explorar paso a paso el proceso seguido para lograr el proyecto, por lo tanto es suficiente con ir ejecutanto celda tras celda según sea el interés del usuario.

Consideraciones
- Se toma en cuenta que el dataset está listo con cada clase separada en su propia carpeta. 

-----------------------------    
## Anexos

Referencias
- https://deeplizard.com/learn/video/k63bRldLxGI
- https://deeplizard.com/learn/video/INaX55V1zpY
- https://deeplizard.com/learn/video/HDom7mAxCdc
