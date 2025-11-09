# 🤖 Environment E1 y Robotica Cuantica

<img width="3698" height="2326" alt="image" src="https://github.com/user-attachments/assets/7a98b1ce-97d3-4133-a34a-d7a467c1feaf" />


Mediante conocimientos de Docker y Pybullet se busca realizar un despliegue de un Robot Insdustrial del Repositorio de [Pybullet Industrial Robotics Gym]([https://pages.github.com/](https://github.com/rparak/PyBullet_Industrial_Robotics_Gym)).

### ⚙️ ***Desarrollo del Despliegue***

Para realizar el despliegue es importante seguir los siguientes pasos.

1. Copiar el Repositorio de Git.

```
git clone https://github.com/rparak/PyBullet_Industrial_Robotics_Gym.git
cd PyBullet_Industrial_Robotics_Gym
```
<img width="736" height="70" alt="Captura desde 2025-11-08 11-42-23" src="https://github.com/user-attachments/assets/3b31fc75-5773-4662-ab67-82fa6fd014f8" />


2. Para que el despliegue se desarrolle completamente y sin ningun error, se debe tener encuentas las dependencias necesarias.

```
   Matplotlib
$ ../user_name> conda install -c conda-forge matplotlib

SciencePlots
$ ../user_name> conda install -c conda-forge scienceplots

PyBullet
$ ../user_name> conda install -c conda-forge pybullet

Pandas
$ ../user_name> conda install -c conda-forge pandas

SciPy
$ ../user_name> conda install -c conda-forge scipy

PyTorch, Torchvision, etc.
$ ../user_name> conda install pytorch::pytorch torchvision torchaudio -c pytorch
or 
$ ../user_name> conda install pytorch-nightly::pytorch torchvision torchaudio -c pytorch-nightly

Stable-Baselines3
$ ../user_name> conda install -c conda-forge stable-baselines3

Gymnasium
$ ../user_name> conda install -c conda-forge gymnasium
```

***📎 Por problemas de conexion del xhost de la computadora, se opto por desplegar el pybullet mediante Simulación de VNC***

VNC es un servidor (Virtual Network Computing), el cual permite medinate software controlar un ordenador remoto atravez de una red.

3. Teniento encuenta lo anterior, se instala la base de soporte del VNC y lo corremos mediante un contenedor. Para ingresar al servidor lo unico que hacemos es abrir medainte el navegador el contenedor del servidor. `http://localhost:6080` -> **Los ultimos numeros dependeran del servidor creado**

```
sudo docker pull dorowu/ubuntu-desktop-lxde-vnc
sudo docker run -it -p 6080:80 dorowu/ubuntu-desktop-lxde-vnc
```
<img width="1845" height="1017" alt="Captura desde 2025-11-08 11-39-59" src="https://github.com/user-attachments/assets/33635e57-ed9b-4184-95da-4c25cbb16ad0" />

Ya dentro del servidor podremos ver una interfaz del servidor virtual, para empezar el despligue debemos acceder a la terminal del servidor.

<img width="392" height="251" alt="Captura desde 2025-11-08 11-40-07" src="https://github.com/user-attachments/assets/cdbf4516-be34-482c-971e-33eea74781c8" />

<img width="705" height="483" alt="Captura desde 2025-11-08 11-40-15" src="https://github.com/user-attachments/assets/b38e54b5-4454-47d9-9308-412f79fbbd27" />


4. Dentro de la terminal instalaremos el pybullet, las dependencias necesarias y la clonación del repositorio

```
sudo apt update
sudo apt install -y python3-pip git
pip install pybullet numpy
```

5.Para ya poder iniciar el despliegue, solo debemos acceder a la carpeta de `Training` y desplegar el PyBullet del prototipo E1.

<img width="891" height="177" alt="Captura desde 2025-11-08 11-42-54" src="https://github.com/user-attachments/assets/1278b661-a9b2-4c2e-9c80-47a5dcea30ce" />

📎***Resultados Despliegue***

<img width="1854" height="1048" alt="Captura desde 2025-11-07 20-54-26" src="https://github.com/user-attachments/assets/fc732314-ff10-4237-aae5-b43069300758" />

---------------------------------------------

<img width="1721" height="869" alt="Captura desde 2025-11-07 20-55-51" src="https://github.com/user-attachments/assets/63c3505c-4319-4b11-a3b0-adcfb5386a61" />

---------------------------------------------

<img width="1034" height="787" alt="Captura desde 2025-11-07 20-55-44" src="https://github.com/user-attachments/assets/cd1d194d-d22c-4682-b49f-dd0a3d8d8d87" />

---------------------------------------------

### 🧠 Analisis Tecnológica

En la actualidad, la tecnología cuántica está avanza muy rápido, donde su integración con los sistemas digitales y la robótica está generando un nuevos desarrollos tecnológicos. Esta union permite optimizar el procesamiento de datos, mejorar la precisión en los sistemas de control y abrir el camino hacia robots inteligentes con capacidades cuánticas, capaces de resolver problemas complejos con una eficiencia sin precedentes. En esta parte dare a conocer 5 aptentes que fijan un rumbo a la implementación de sistemas cuanticos a la industria.

## QUANTUM-ASSISTED MACHINE LEARNING WITH TENSOR NETWORKS - APRENDIZAJE AUTOMÁTICO ASISTIDO POR CUANTICA CON REDES TENSOR

<img width="500" height="800" alt="image" src="https://github.com/user-attachments/assets/5cc6ea61-7f28-492b-84b2-0c85cc0d3763" />


Un método de aprendizaje automático asistido por computación cuántica consiste en codificar datos clásicos en múltiples estados cuánticos mediante el uso de un mapa de codificación aplicado por un circuito de procesamiento. Posteriormente, se entrena un modelo cuántico basado en dichos estados cuánticos, el cual puede estar estructurado como una red tensorial.
Además, el método contempla la compilación del modelo cuántico en un circuito cuántico, asignando qubits virtuales a qubits físicos dentro de un dispositivo de hardware cuántico, donde el circuito resultante incluye una secuencia de operaciones optimizadas para ejecutarse en dicho hardware cuántico.

## OPTIMIZING QUANTUM COMPUTING CIRCUIT STATE PARTITIONS FOR SIMULATION - OPTIMIZACIÓN DE LAS PARTICIONES DEL ESTADO DE LOS CIRCUITOS DE COMPUTACIÓN CUÁNTICA PARA LA SIMULACIÓN

<img width="1000" height="900" alt="image" src="https://github.com/user-attachments/assets/d42b7f84-d4e4-46dd-ab1c-1cf41ea16b12" />


Diversos sistemas y métodos permiten optimizar las particiones de estado de circuitos de computación cuántica destinadas a la simulación. En este enfoque, el estado cuántico de un circuito puede representarse mediante una o varias particiones de vectores de estado. Para mejorar el rendimiento, se aplican algoritmos de agrupamiento de compuertas, análisis de complejidad de compuertas y optimización del orden de los qubits.
Estas particiones se evalúan en función del perfil topológico de la plataforma de cómputo mediante una función de evaluación de costos, la cual estima la eficiencia de ejecución según los recursos de procesamiento disponibles en la plataforma de simulación. Finalmente, las particiones optimizadas del vector de estado se transfieren a dicha plataforma para simular el circuito cuántico con el máximo aprovechamiento computacional.

## Ion-Trapping Quantum Computing Task Execution - Ejecución de tareas de computación cuántica mediante captura de iones

<img width="1875" height="939" alt="image" src="https://github.com/user-attachments/assets/1a7966bb-cb9d-4ac0-96d7-08f176ad1cca" />


Este método implementado por computadora describe la ejecución de tareas de computación cuántica mediante un sistema cuántico basado en iones atrapados. El proceso inicia al recibir una solicitud de un cliente cuántico para ejecutar una tarea específica en el sistema cuántico. Posteriormente, el sistema realiza la tarea solicitada atrapando y manipulando un conjunto de iones, los cuales representan los qubits físicos utilizados en el cálculo. Finalmente, el sistema envía una respuesta con los resultados de la tarea cuántica ejecutada al cliente, cerrando el ciclo de procesamiento y comunicación cuántica.

## A Predictive Control Method of Space Robot Based on Quantum Particle Swarm Optimization - Método de control predictivo de robots espaciales basado en la optimización cuántica de enjambres de partículas

<img width="1000" height="622" alt="image" src="https://github.com/user-attachments/assets/c41c7d3b-c1c4-4a33-b8dd-c67a5b487e80" />


La invención propone un método de control predictivo para robots espaciales basado en un algoritmo cuántico de enjambre de partículas. El proceso inicia con la formulación de un modelo dinámico lagrangiano del robot espacial, que se combina con un modelo cinemático para obtener un modelo de espacio de estados discretizado.
Posteriormente, se diseña un controlador predictivo discreto que utiliza polinomios de Laguerre y optimiza el rendimiento mediante el algoritmo cuántico de enjambre de partículas, corrigiendo errores de predicción de forma continua. Este enfoque permite seguir trayectorias objetivo con alta precisión, reducir el consumo energético y evitar limitaciones de los métodos convencionales de programación cuadrática bajo múltiples restricciones.

## Clock synchronization system, signal synchronization control method and storage medium - Sistema de sincronización de reloj, método de control de sincronización de señales y medio de almacenamiento

<img width="1000" height="486" alt="image" src="https://github.com/user-attachments/assets/c6b9b894-21b5-44af-acb2-4f554f9c0eba" />

Esta invención presenta un sistema de sincronización de reloj que combina un procesador de control cuántico con un convertidor digital-analógico (DAC). El DAC incorpora módulos de conversión de frecuencia y sincronización de señal, utilizando un disparador tipo D para alinear las señales.
El procesador cuántico genera una señal de sincronización global y una señal de reloj de referencia, las cuales se procesan para obtener una señal de reloj objetivo sincronizada con alta precisión. Gracias al disparador D, el sistema reduce el retardo de señal y mejora la exactitud de la sincronización, garantizando una operación estable en entornos cuánticos y digitales.


### REFERENCIAS

- IBM. (2022). Quantum-assisted machine learning (Patente No. US2022108218A1). European Patent Office. Disponible en https://worldwide.espacenet.com/patent/search?q=pn%3DUS2022108218A1
- NVIDIA Corp. (2024). Optimizing quantum computing circuit state partitions for simulation (Patente No. US2024311668A1). European Patent Office. Disponible en https://worldwide.espacenet.com/patent/search?q=pn%3DUS2024311668A1
- Honeywell International Inc. (2023). Computer-implemented method for executing a quantum computing task (Patente No. US2023244981A1). European Patent Office. Disponible en https://worldwide.espacenet.com/patent/search?q=pn%3DUS2023244981A1
- Beijing Institute of Technology. (2020). Quantum particle swarm algorithm-based space robot predictive control method (Patente No. CN107662211B). Google Patents. Disponible en https://patents.google.com/patent/CN107662211B/en?q=(Quantum+robotics)&oq=Quantum+robotics
- University of Science and Technology of China. (2022). Clock synchronization system based on quantum control processor and digital-to-analog converter (Patente No. CN113132077B). Google Patents. Disponible en https://patents.google.com/patent/CN113132077B/en?q=





