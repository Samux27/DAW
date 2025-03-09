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

Actividad 5
![image](https://github.com/user-attachments/assets/34673bca-38aa-4c32-bf7a-b66ff29f2405)

Actividad 6
![image](https://github.com/user-attachments/assets/603d4da6-c2f3-40d4-891c-2a42292d91e4)
