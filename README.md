# PC3_MachineLearning

**Objetivo de la Implementación**

El propósito de esta implementación es capacitar al Robot NAO con capacidades interactivas basadas en inteligencia artificial, permitiéndole llevar a cabo una actividad entretenida que combina un test de preferencias de género de películas con una rutina de baile. Esta actividad tiene como fin no solo evaluar las preferencias de los usuarios mediante un test interactivo, sino también ofrecer una respuesta animada en forma de baile, haciendo uso de Python. En este proyecto, el Robot NAO enuncia afirmaciones sobre distintos géneros de películas, y los usuarios puntúan cada una en una escala del 1 al 5 según su afinidad, para luego recibir un top 3 de géneros de películas que mejor se alinean con sus intereses.

**Descripción de los Componentes de la Arquitectura de la Implementación**

1. Test Interactivo de Preferencias de Género de Películas en Python
   
El test se diseñó para que el Robot NAO enuncie afirmaciones específicas sobre diferentes géneros de películas, utilizando código en Python. Cada afirmación está relacionada con un género en particular, y el usuario responde con un puntaje del 1 al 5, indicando su nivel de identificación. Este puntaje se acumula para calcular una afinidad total hacia cada género.
- Proceso:
El robot enuncia cada afirmación y solicita al usuario que responda con un puntaje del 1 al 5.
Los puntajes se almacenan a cada género, cada género tiene un peso distinto para cada afirmación.
Al finalizar, se suman los puntajes de cada género y se determina el top 3 de géneros preferidos.
- Entradas: Respuestas numéricas del usuario (1 a 5) para cada afirmación.
- Salida: Top 3 de géneros de películas preferidos por el usuario.
- Implementación: El test está desarrollado en Python, gestionando las respuestas en tiempo real y acumulando puntajes en arreglos para cada género.

2. Comunicación entre el Test y el Robot NAO
   
El script en Python permite al Robot NAO recibir las respuestas del usuario para cada afirmación y almacenar los puntajes correspondientes. Este facilita la acumulación de puntajes y determina el top 3 de géneros al final del test.
- Proceso:
El robot recibe el puntaje ingresado por el usuario y lo asigna al género correspondiente.
Al finalizar, el robot muestra los tres géneros más afines con el usuario.

4. Coreografía de Baile
   
La coreografía se implementó utilizando Python, controlando los movimientos del Robot NAO mediante comandos específicos de la API. Esta secuencia coreográfica se activa en respuesta a los resultados del test, sirviendo como acción final del mismo y basada en movimientos predefinidos.
- Composición: Cada paso del baile se define mediante comandos que indican las posiciones de las articulaciones del robot, creando una rutina sincronizada.
Ejecución: Una vez que se presentan los géneros seleccionados, el robot ejecuta el baile para finalizar la interacción de manera lúdica.

5. Simulador NAO
   
Descripción: El simulador se utiliza para verificar el funcionamiento del test y la coreografía sin necesidad del hardware físico. Es útil para probar tanto la comunicación de datos entre el test y el robot como para visualizar la coreografía final.

**Instrucciones de Instalación del Modelo de IA en el Robot NAO**

1. Configuración del entorno
- Se debe tener instalado Python y las bibliotecas necesarias como NAOqi.
- Se configura el entorno de desarrollo con los SDK de NAO.
  
2. Carga del Script en el Robot:
- Se carga el script del modelo de IA en el Robot NAO utilizando el software de programación de NAO.
- El robot tiene que estar conectado a la misma red que tu ordenador.
  
3. Ejecutar el Script
- Se inicia el script en el Robot NAO y verifica que el robot se coloque en la postura inicial.
- Se realizan pruebas interactivas del test de preferencias y de la coreografía para asegurar que ambos componentes funcionen correctamente.

4. Depuración
- Si surgen problemas, se revisan los logs de salida y se ajusta el código según sea necesario.
