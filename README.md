# Proyecto Integrador 2
-----------------------------
Equipo #6

Integrantes:

    - Alexis Ruiz Bernadac
    - Oswaldo Silva Ruelas
    - Diego Fernando Valencia Martínez
    - Juan Pablo Vargas Rodríguez
    - Kevin Eduardo Aguilar Escayola

-----------------------------
## ¿Qué hace el proyecto?

Se realiza una implementación de YOLOv3 junto con diversas técnicas de visión computacional para realizar un sistema de monitoreo de sana distancia. Se combina la eficacia y rapidez de detección de esta arquitectura junto con la habilidad de TensorFlow para optimizar recursos computacionales y dar soporte a módulos como GPUs. Entonces, se utiliza el reconocimiento de la clase persona para obtener los individuos dentro de la escena y a partir de sus centros estimar la distancia que hay entre ellos. No obstante, se encontró tempranamente la limitante implicada por la pose de la cámara y la falta de abstracción de profundidad. Para aumentar la robustez del sistema respecto a esto, se realizó una homografía a partir de cuatro puntos tomados de la escena original y sus cuatro correspondientes dentro de un plano bidimensional. Esto permitió contar con una matriz de transformación que puede utilizarse para intepretar la posición de las personas de modo que se considere sutilmente su profundidad. Por último, se utiliza una implementación de tracking mediante Deep Sort facilitada por: https://www.youtube.com/watch?v=Cf1INvUsvkM

-----------------------------        
## ¿Cuál es la importancia del proyecto?

Dada la crisis sanitaria actual ocasionada por SARS-CoV-2, se ha evidenciado que el mejor recurso para combatir la propagación es el distanciamiento social. No obstante, es una realidad que tarde o temprano deberá regresarse a actividades cotidianas, y entonces deberá asumirse una normalidad donde se evite la congregación de varias personas. Esto implica la necesidad de promover una distancia entre transeúntes, coloquialmente conocida en México como "Susana Distancia". Por todo lo anterior, un sistema como el descrito con anterioridad resultaría muy útil para poder detectar las zonas en entornos urbanos donde se infrinja con mayor frecuencia la sana distancia, y entonces se tomen acciones específicas para combatirlo. 

-----------------------------    
## Funcionamiento

Para utilizar el sistema se recomienda utilizar el siguiente comando:

    python object_tracker.py --video ./data/video/test.mp4 --output ./data/video/results.mp4 --output_format mp4v
    
Consideraciones:
        
- El detector incluye diferentes argumentos que permiten customizar la ejecución del programa. Estos están basados en: https://github.com/theAIGuysCode/yolov3_deepsort
- Una limitante de la solución obtenida es el proceso de calibración que debería realizarse para diferentes poses de la cámara o diferentes escenas. Por lo tanto, de momento el sistema está preparado de momento para el video test.mp4 tomado del dataset Oxford Town Centre. 

-----------------------------    
## Anexos

Las principales fuentes de inspiración para este proyecto:

- https://landing.ai/landing-ai-creates-an-ai-tool-to-help-customers-monitor-social-distancing-in-the-workplace/
- https://github.com/theAIGuysCode/yolov3_deepsort
- https://github.com/theAIGuysCode/tensorflow-yolov4-tflite

Recursos adicionales:

- https://www.learnopencv.com/homography-examples-using-opencv-python-c/
- https://github.com/ParthPathak27/Social-Distancing-Detector
- https://docs.opencv.org/2.4/modules/calib3d/doc/camera_calibration_and_3d_reconstruction.html
- https://docs.opencv.org/2.4/modules/imgproc/doc/geometric_transformations.html
- https://pjreddie.com/darknet/yolo/