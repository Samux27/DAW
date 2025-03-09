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
<img width="1095" alt="Sin título" src="https://github.com/user-attachments/assets/5af00579-ceb8-4d26-a24f-f8d6c0c8fd41" />

Actividad 2
![image](https://github.com/user-attachments/assets/f207e95e-1ea8-4042-807b-ba386b453a4f)

Actividad 3
![image](https://github.com/user-attachments/assets/21488ea3-de77-4ccb-936f-5d3eb81a42da)

Actividad 4
![image](https://github.com/user-attachments/assets/1f967108-4dc5-48b7-88b4-80f6d104782d)

Actividad 5
![image](https://github.com/user-attachments/assets/34673bca-38aa-4c32-bf7a-b66ff29f2405)

Actividad 6
![image](https://github.com/user-attachments/assets/603d4da6-c2f3-40d4-891c-2a42292d91e4)
