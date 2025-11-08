# 🤖 Environment E1 

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

<img width="1034" height="787" alt="Captura desde 2025-11-07 20-54-44" src="https://github.com/user-attachments/assets/a530d3c0-218a-4d8a-9c95-60addcc62278" />






