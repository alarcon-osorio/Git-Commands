##SSH  -- Pasos Preliminares

1. La creacion de la llave publica y privada se puede hacer con Putty Keygen

2. Copiar contenido de id_rsa.pub --> Creada en la ruta opc/
   En PC usado
  
3. Ese contenido se pega en la opciones de GITHUB SSH And GPG Keys

Generar una nueva clave SSH
Abre el terminal Git Bash.

Pega el siguiente texto, que sustituye tu dirección de correo electrónico en GitHub Enterprise.

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Esto crea una nueva clave ssh usando el correo electrónico proporcionado como etiqueta.
