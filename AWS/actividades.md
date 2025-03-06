
Creamos las VPC necesarias dentro y luego accedemos a AWS 
crearemos 2 publicas y 2 privadas

![image](https://github.com/user-attachments/assets/110d3ebc-2772-42e4-824a-320398ec7a56)
Entramos en la vpc para crear las instancias 
![image](https://github.com/user-attachments/assets/2e7cecf8-28bb-44e0-b377-ea042035d25b)
Y creamos las vpc con los siguientes parametros 
Nombre del VPC: wordpress-vpc.

Bloque CIDR IPv4: 10.0.0.0/16.

Bloque CIDR IPv6: Opcional .

Tenencia: Predeterminado
![image](https://github.com/user-attachments/assets/06fc1f87-fa0a-4d43-a952-bd950aa9cd0d)
Y ahora debemos crear las subredes 
![image](https://github.com/user-attachments/assets/f51d79d3-92a6-4c30-aec1-84678b993a74)
y las configuramos con los parametros que se muestran 
![image](https://github.com/user-attachments/assets/bc5b9031-8438-49fe-85b6-60c78e2f0059)
y tambien para la segunda subred publica 
![image](https://github.com/user-attachments/assets/9ace1b41-6c91-42b5-83cd-f8d070caba20)
y las privadas 
![image](https://github.com/user-attachments/assets/9d5bd98f-13b5-478b-bf5c-fc59419b4a6a)
![image](https://github.com/user-attachments/assets/05bf105f-de4b-4c97-a831-17f2c21f3479)

Y ahora configuramos las puertas de enlaces 
![image](https://github.com/user-attachments/assets/35b80d23-5209-430d-8e08-63a4f2bf5c89)
![image](https://github.com/user-attachments/assets/922be5aa-37d7-4e1d-a2ab-c6193cae0448)
y una vez creada la contectamos a la vpc creada anteriormente 
![image](https://github.com/user-attachments/assets/997f28b0-4d03-44a6-805f-f565f9a4d9b0)
y creamos las tablas de enrutamiento
![image](https://github.com/user-attachments/assets/128a9e8e-7b2d-4df7-8da3-5650d1357159)
Renombramos y asi deberian quedar nuestras tablas de enrutamiento 
![image](https://github.com/user-attachments/assets/3fc5f617-a7aa-493c-830c-144f59f908ff)
ahora modificamos las publicas ![image](https://github.com/user-attachments/assets/0f0009a3-5cd6-4108-a3dd-84fe309d6287) y añadimos a las rutas el 0.0.0.0/0 como ruta de internet y selecionamos nuestro gateway y guardamos 
![image](https://github.com/user-attachments/assets/0424f0dc-7a54-48b3-b227-2e7230a48fcb)

selecionamos la tabla publica y vamos al apartado de asociar subredes y añadimso solo las publicas y hacemos lo mismo con las privada 
![image](https://github.com/user-attachments/assets/88d6c32f-888b-4661-a7e5-65ebf0664b89)

![image](https://github.com/user-attachments/assets/0442d77b-c2ad-4f72-a927-03e8cd8c4ae9)

Una vez configurada las subredes vemos que han cambiado el campo de asociaciones 
![image](https://github.com/user-attachments/assets/1f97dbee-73b9-4859-ae53-3ebbc0184e0c)

ahora accdemos al apartado de Ec2 para crear la instancia de la maquina virtual.
![image](https://github.com/user-attachments/assets/4ad830bf-7431-4fde-a217-39a1f98aa1d1)
y lanzamos una instancia con la imagen ubuntu con la siguiente configuracion 
![image](https://github.com/user-attachments/assets/eb591709-7d48-4d6d-a487-751a58f6fe66)
 ![image](https://github.com/user-attachments/assets/e1258fa5-d335-4466-a4e4-69464927e3f9)
![image](https://github.com/user-attachments/assets/4137ccfc-46f5-4f21-af42-e5dd06bf4c8f)
una vez terminemos la configuracion iniciamos la instancia y nos conectamos 
![image](https://github.com/user-attachments/assets/94617cf4-42b7-4751-a263-375b6eb075f0)
actualizamos los paquetes con sudo apt update y upgrade. 
instalamos apache 
![image](https://github.com/user-attachments/assets/01029cac-bde3-46b5-a927-fbcfe288223a)
y lo iniciamos 
![image](https://github.com/user-attachments/assets/3f23176e-e1ce-424e-8198-fe98dbfff2df)
instalamos php 
![image](https://github.com/user-attachments/assets/1068c129-b68f-4890-ad96-f0c131fee236)
![image](https://github.com/user-attachments/assets/7b12c769-91de-4d14-b147-bae7c1f751cc)

y comprobamos con la siguiente ruta http://ec2-34-192-84-9.compute-1.amazonaws.com/info.php
![image](https://github.com/user-attachments/assets/e9ecc839-2440-4da8-98c1-55c0e1aa9e5a)
Servicios RDS
![image](https://github.com/user-attachments/assets/d3ed4ae0-e308-454b-a4dd-ba6c7dc79593)
Creamos una base de datos con mysql 
![image](https://github.com/user-attachments/assets/f67ed552-c0cc-4383-9d75-4418b0c763d0)
![image](https://github.com/user-attachments/assets/2ac805d8-f03d-4b1d-b002-658bc93d863f)
Creamos un sistema de archivos 
![image](https://github.com/user-attachments/assets/ff7824ee-4902-45a8-9d71-dd18055a5064)
![image](https://github.com/user-attachments/assets/f7f8d8d4-29a1-4b0d-a69b-fd466e3feda2)
![image](https://github.com/user-attachments/assets/2bf04434-e1aa-409b-b440-324d5b44d732)
sudo apt install nfs-common 
![image](https://github.com/user-attachments/assets/06bcd51e-e33b-4d53-9a5a-0cac71925128)
descargamos he instalamos wordpress cd /var/www/html sudo wget http://wordpress.org/latest.tar.gz sudo tar -xzf latest.tar.gz
![image](https://github.com/user-attachments/assets/16e7e24c-ba98-4fc1-af5d-f211c976159f)

configuramos la base de datos para worpress: sudo nano wp-config.php define( 'DB_NAME', 'nombre_de_la_base_de_datos' ); define( 'DB_USER', 'nombre_de_usuario' ); define( 'DB_PASSWORD', 'contraseña_del_usuario' ); define( 'DB_HOST', 'localhost' ); Reemplaza los valores entre comillas con la información correcta de tu base de datos RDS:

DB_NAME: El nombre de tu base de datos en RDS

DB_USER: El nombre de usuario de la base de datos

DB_PASSWORD: La contraseña de la base de datos

DB_HOST: El punto de enlace de tu instancia RDS Nos conectamos a la instancia de la base de datos .Creamos Base de datos, usuario y contraseña: CREATE DATABASE wordpress; CREATE USER 'wordpress_user'@'%' IDENTIFIED BY 'password123'; GRANT ALL PRIVILEGES ON wordpress.* TO 'wordpress_user'@'%'; FLUSH PRIVILEGES;
![image](https://github.com/user-attachments/assets/59bb1330-8a9b-4057-9c14-1c91a5696e92)
![image](https://github.com/user-attachments/assets/1388c93a-df8c-48a3-9ce5-aafab46e405c)
Lanzamos la instalación simplemente llamando al servidor web en el navegador:http://22.133.41.132/wordpress

![image](https://github.com/user-attachments/assets/50ec9264-1856-436a-b0dd-7f4b841d2069)
y Simplemente realizamos una instalacion basica de wordpress como ya hemos realizado anteriormente
![image](https://github.com/user-attachments/assets/9c29ea81-55ae-4c9e-a248-f08261d21d13)
![image](https://github.com/user-attachments/assets/ea06b4e9-0a9b-4692-a7de-90b006bfc7d7)


