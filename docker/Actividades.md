Actividad 0
![image](https://github.com/user-attachments/assets/8f4de827-50ad-40cd-b86a-a5b4136dca2f)

Actividad 1
![image](https://github.com/user-attachments/assets/2879ec04-4304-4ca1-804e-a3393fbddd5f)
hacer el set-up del repositirio de docker.
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
Y añadimos el repositio en el apt
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] \
https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" \
| sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt-get update

![image](https://github.com/user-attachments/assets/9a8267a9-89b5-4b5e-a433-bbd03eb32546)
Instalamos los paquetes de docker 


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

![image](https://github.com/user-attachments/assets/56eb823b-6930-4cc0-9f91-fab930b94049)
Y Comprobamos que todo funcione correctamente

![image](https://github.com/user-attachments/assets/7a8eeaa6-4b8c-413d-98e4-fa98ff5a8a1d)

Actividad 2

![image](https://github.com/user-attachments/assets/f207e95e-1ea8-4042-807b-ba386b453a4f)
ya hemos mostrado la imagen hello-word anteriormente con el comando 
sudo docker run hello-world
 Y para mostrar las imagenes creadas usamos :
sudo docker images
y para ver los contonedores: 
sudo docker ps
para verlo todo es con :
docker ps -a
Creamos y Editarmos un dockerfile

![image](https://github.com/user-attachments/assets/acd6694a-ce75-4b7c-9924-8e76fd1e0e61)
Y colocamos algo basico dentro:

![image](https://github.com/user-attachments/assets/3878b7a9-b08f-4819-8172-e2a2bff802a0)
y cremos el contenedor con el comando 

![image](https://github.com/user-attachments/assets/489c93bf-9c8b-4ad6-8a2f-d03cb7785c2c)

![image](https://github.com/user-attachments/assets/4cbae1f1-948d-4b7c-b574-c8e0f844b66e)
y para correrlo hacemos 
sudo docker run proyecto

![image](https://github.com/user-attachments/assets/4a2cef1f-d8ce-4389-bd22-b47ed6b54378)


Creamos una cuenta en hub.docker.com

![image](https://github.com/user-attachments/assets/417f2e53-4a9b-45cf-aba4-4d31f7328a99)
cremos un repositorio en la web y hacemos docker login 

![image](https://github.com/user-attachments/assets/66517fa0-142e-4956-b356-7c51ca392382)
Despues debemos etiquetar el proyecto para que tenga la misma etiqueta que mi usuario de dockerhub. por ejemplo yo usare 
docker tag proyecto samux27/proyecto:latest

![image](https://github.com/user-attachments/assets/b84e3574-25cd-4d30-881d-da2c0cf25c00)
y ahora lo subimos al repositorio. con 
docker push samux27/proyecto:latest
y comprobamos que se haya subido a nuestro repostirio 

![image](https://github.com/user-attachments/assets/a29581bb-062f-422a-8cb8-789db4ef226f)

Actividad 3

![image](https://github.com/user-attachments/assets/21488ea3-de77-4ccb-936f-5d3eb81a42da)
Para descargar las imagenes de ubuntu, hello-word y Ngix ejecutamos los siguientes comandos respectivamente 

![image](https://github.com/user-attachments/assets/1c41f9a2-ba26-4280-8236-97751ce77b62)

![image](https://github.com/user-attachments/assets/8a002d5e-a0c9-4e6d-b37c-9d64702eaced)

![image](https://github.com/user-attachments/assets/4a9a6d29-171e-4178-86fd-5c562992a060)
y ejecutando el sigueinte comando podemos ejecutar el contenedor y darle un nombre 

![image](https://github.com/user-attachments/assets/727e698a-c078-464a-983f-3c31b0f2b904)

![image](https://github.com/user-attachments/assets/3a12b887-19d1-4b1a-8583-1bfddbcdc0de)
y los mismos para los siguientes 
![image](https://github.com/user-attachments/assets/fe2a2bfa-365b-47f9-976f-ab9afbaa3732)
![image](https://github.com/user-attachments/assets/a68c35db-7c25-43aa-b9da-9392104b3e2f)
Paramos los contenedores con 

![image](https://github.com/user-attachments/assets/4cff9c81-c24b-48b9-80bb-2ce6c449b094)
Y los eliminamos con 

![image](https://github.com/user-attachments/assets/afa1b6f4-c8f3-421a-ac32-558ddc7989c1)

![image](https://github.com/user-attachments/assets/9d604010-de26-4039-a14d-ebd005e144b9)

![image](https://github.com/user-attachments/assets/ec3344f5-2080-4c01-9376-088ce865e63e)

Actividad 4
![image](https://github.com/user-attachments/assets/1f967108-4dc5-48b7-88b4-80f6d104782d)
La aplicación guestbook se conecta por defecto a la base de datos utilizando el nombre redis, por lo que es necesario asignar ese mismo nombre al contenedor de Redis para garantizar una correcta resolución de nombres.

Es fundamental que ambos contenedores estén dentro de la misma red y puedan comunicarse mediante nombres (DNS), ya que no se puede predecir de antemano qué dirección IP se asignará a cada uno. Por ello, crearemos ambos contenedores en la misma red.

docker network create red_guestbook

![image](https://github.com/user-attachments/assets/23a9c187-5149-4c20-8f66-167fca45190e)
Para ejecutar los contenedores:


![image](https://github.com/user-attachments/assets/2881e365-9b67-4fef-8409-9f6ee30d4d8b)

![image](https://github.com/user-attachments/assets/8ddc748f-d841-4fa1-b979-e67dba2092c6)
y para comprobar que todo funciona correctamente buscamos localhost 

![image](https://github.com/user-attachments/assets/de0fac5e-cd1a-4dc6-b577-0e997e6a0033)
EJEMPLO 2 - Despliegue de la aplicación Temperaturas
Vamos a crear una red para conectar los dos contenedores:

![image](https://github.com/user-attachments/assets/fb022fd3-a593-4a81-abc5-3c7936a20e08)

y Ejecutamos los contenedores

![image](https://github.com/user-attachments/assets/b97cd721-25e8-4a37-91f2-33b1e28cbf7a)

![image](https://github.com/user-attachments/assets/3f440258-a293-4c90-a48f-8b94dcec425c)
docker run -d -p 80:3000 --name temperaturas-frontend --network red_temperaturas iesgn/temperaturas_frontend
Y si accedemos a localhost podemos comprobar que la aplicacion esta 

![image](https://github.com/user-attachments/assets/ef9cedb1-7596-4e1c-a964-bafd69f34d37)
EJEMPLO 3 - Despliegue de Wordpress + mariadb
Para instalar WordPress se requieren dos contenedores: uno para la base de datos (utilizando la imagen de MariaDB) y otro para el servidor web que aloja la aplicación (utilizando la imagen de WordPress). Ambos contenedores deben estar en la misma red y poder comunicarse mediante nombres (resolución DNS), ya que no sabemos qué dirección IP se asignará a cada uno. Por esta razón, crearemos los contenedores dentro de la misma red.

docker network create red_wp
![image](https://github.com/user-attachments/assets/fe1fa3b7-94cb-4119-9922-5419397ce6c1)

Viendo la documentacion de la imagen de mariadb y la imagen de wordpress podemso ejecutar los siguiente comandos

![image](https://github.com/user-attachments/assets/631eb8f9-f008-43e5-865e-ad37da01a891)
![image](https://github.com/user-attachments/assets/c7988cb4-c80d-4ebf-8345-350bdabf239d)
 Una vez ejecutados los comandos podemos comprobar los contenedores y si visitamos localhost.
 ![image](https://github.com/user-attachments/assets/8879e54a-c3ea-454b-8d6c-db79d923c053)

Actividad 5
![image](https://github.com/user-attachments/assets/34673bca-38aa-4c32-bf7a-b66ff29f2405)

Actividad 6
![image](https://github.com/user-attachments/assets/603d4da6-c2f3-40d4-891c-2a42292d91e4)
EJEMPLO 1 - Construcción de imágenes con una página estática

En este ejemplo vamos a crear una imagen con una página estática. Vamos a crear tres versiones de la imagen.
Tenemos un directorio, que en Docker se denomina contexto, donde tenemos el fichero Dockerfile y un directorio, llamado public_html con nuestra página web:
ls Dockerfile  public_html

![image](https://github.com/user-attachments/assets/d80ad634-3ff7-4bee-8f81-4a5b7b89f106)
En este caso vamos a usar una imagen base de un sistema operativo sin ningún servicio. El fichero Dockerfile será el siguiente:
![image](https://github.com/user-attachments/assets/96c5daa2-001a-4566-926f-a9776cd91f3b)
Al utilizar la imagen base debian:stable-slim, es necesario instalar los paquetes requeridos para configurar el servidor web, en este caso apache2. Posteriormente, se añadirá el contenido del directorio public_html en la ruta /var/www/html/ dentro del contenedor. Finalmente, se especificará el comando que debe ejecutarse al iniciar un contenedor basado en esta imagen: se pondrá en marcha el servidor web en segundo plano.
y Para crear la imagen usamos docker build -t samux27/ejemplo1:v1 .
![image](https://github.com/user-attachments/assets/4d7f16e4-855e-4cef-b253-4ec6029653f0)
Visito localhost y vemos 
![image](https://github.com/user-attachments/assets/2ddd904c-151e-48e3-82aa-ceb253fee4ec)
EJEMPLO 2 - Construcción de imágenes con una una aplicación PHP

En el contexto voy a tener el fichero Dockerfile y un directorio, llamado app con mi aplicación.

En este caso voy a usar una imagen base de un sistema operativo sin ningún servicio. El fichero Dockerfile será el siguiente:
![image](https://github.com/user-attachments/assets/a791ef08-1527-4e36-b9dc-961e5d032fd0)
y creamos la imagen con docker build -t samux27/ejemplo2:v1 .
![image](https://github.com/user-attachments/assets/1f04e404-dff9-4c32-82d0-2ec7131b1c7b)

Y comprobamos en localhost 
![image](https://github.com/user-attachments/assets/f8865da2-4849-49b1-943c-e6aebc0fa513)
EJEMPLO 3 - Construcción de imágenes con una una aplicación Python
He descargado la versión 1 del repositorio https://github.com/josedom24/curso_docker_ies/tree/main/ejemplos/modulo5/ejemplo3/app para llevar a cabo esta actividad.
En este ejemplo, crearé una imagen destinada a servir una aplicación desarrollada en Python utilizando el framework Flask. Dicha aplicación se ejecutará en el puerto 3000/tcp.
El contexto del proyecto incluirá el archivo Dockerfile y un directorio llamado app que contendrá la aplicación.
En este caso, utilizaremos una imagen base de un sistema operativo sin servicios preinstalados. El contenido del archivo Dockerfile será el siguiente:
![image](https://github.com/user-attachments/assets/e8d1c2d2-72a9-4304-a88e-4b6d6f4a258e)
y creamos la imagen 
docker build -t samux27/ejemplo3:v1 .
![image](https://github.com/user-attachments/assets/9d3a1f60-ece7-4226-bddb-7893f0d75f10)
docker run -d -p 80:3000 --name ejemplo2 samux27/ejemplo3:v1
![image](https://github.com/user-attachments/assets/ccc86ac3-16b5-4526-9a17-ae79f6ad0876)

