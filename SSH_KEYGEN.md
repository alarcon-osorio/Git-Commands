##SSH  -- Pasos Preliminares

1. La creacion de la llave publica y privada se puede hacer con Putty Keygen

2. Copiar contenido de name_your_key.pub --> Creada en la ruta Server Local
  
3. Ese contenido se pega en las opciones de la cuenta GITHUB(En la foto) --> SSH And GPG Keys

      Pasos alternos para generar una nueva clave SSH
      Abre el terminal Git Bash.

      Pega el siguiente texto, que sustituye tu dirección de correo electrónico en GitHub Enterprise.

      $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
      
      Generating public/private rsa key pair.
      Enter file in which to save the key (/c/Users/alarcon_osorio/.ssh/id_rsa): name_your_key
      Enter passphrase (empty for no passphrase):
      Enter same passphrase again:

      Esto crea una nueva clave ssh usando el correo electrónico proporcionado como etiqueta.

      La crea en la ruta del servidor C:\Users\\nombreUsuario\\.ssh\\nombreLlave
      
      --> Iniciamos la cuenta SSH
      
      eval $(ssh-agent -s) 
      
      Agent pid 793
      
      --> Agregamos la identidad
      
      ssh-add ~/.ssh/name_your_key
      
      Enter passphrase for /c/Users/opc/.ssh/ssh:
      
      Identity added: /c/Users/opc/.ssh/ssh (your_email@example.com)
      
      Probra Conexion 
      
      ssh -T git@github.com
      
4. Volver al paso 2

_Nota: Si al hacer git push no funciona luego de cerrar y abrir Git, realizar estos comandos nuevamente en la ruta local de los repos_
      
      eval $(ssh-agent -s) 
      
      Agent pid 793
      
      --> Agregamos la identidad
      
      ssh-add ~/.ssh/name_your_key
 
 ----------------------------------------------
 
_Repos Nuevos_

echo "# Android" >> README.md

git init

git add README.md

git commit -m "first commit"

git branch -M main

--- No olvidar ya si es para repos nuevos o existentes olvidaos 

git remote add origin https://github.com/alarcon-osorio/Android.git

git push -u origin main
      

