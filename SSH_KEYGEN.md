##SSH  -- Pasos Preliminares

1. La creacion de la llave publica y privada se puede hacer con Putty Keygen

2. Copiar contenido de id_rsa.pub --> Creada en la ruta opc/
   En PC usado
  
3. Ese contenido se pega en las opciones de la cuenta GITHUB --> SSH And GPG Keys

   Pasos alternos para generar una nueva clave SSH
      Abre el terminal Git Bash.

      Pega el siguiente texto, que sustituye tu dirección de correo electrónico en GitHub Enterprise.

      $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

      Esto crea una nueva clave ssh usando el correo electrónico proporcionado como etiqueta.

      La crea en la ruta del servidor C:\Users\opc\.ssh 
      
      --> Iniciamos la cuenta SSH
      
      eval $(ssh-agent -s) 
      
      Agent pid 793
      
      --> Agregamos la identidad
      
      ssh-add ~/.ssh/ssh
      
      Enter passphrase for /c/Users/opc/.ssh/ssh:
      
      Identity added: /c/Users/opc/.ssh/ssh (alarcon_osorio@hotmail.com)

      

