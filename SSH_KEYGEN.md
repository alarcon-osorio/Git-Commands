##SSH  -- Pasos Preliminares

1. La creacion de la llave publica y privada se puede hacer con Putty Keygen

2. Copiar contenido de id_rsa.pub --> Creada en la ruta Server Local
  
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

      La crea en la ruta del servidor C:\Users\your_user\.ssh 
      
      --> Iniciamos la cuenta SSH
      
      eval $(ssh-agent -s) 
      
      Agent pid 793
      
      --> Agregamos la identidad
      
      ssh-add ~/.ssh/name_your_key
      
      Enter passphrase for /c/Users/opc/.ssh/ssh:
      
      Identity added: /c/Users/opc/.ssh/ssh (your_email@example.com)
      
4. Volver al paso 2

      

