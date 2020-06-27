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

> Generating public/private rsa key pair.
Cuando se te indique "Ingresar un archivo donde guardar la clave", presiona Intro. Al hacerlo aceptas la ubicación predeterminada del archivo.

> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
> Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
Donde se indica, escribe una contraseña segura. Para obtener más información, consulta "Trabajar con frases de contraseña de la clave SSH".
> Enter passphrase (empty for no passphrase): [Type a passphrase]> Enter same passphrase again: [Type passphrase again]

Agregar tu clave SSH al ssh-agent
Antes de agregar una nueva clave SSH al ssh-agent oara gestionar tus claves, debes haber comprobado las claves SSH existentes y generado una nueva clave SSH.
If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys. It also comes with the Git Bash tool, which is the preferred way of running git commands on Windows.

Verifica que el ssh-agent se esté ejecutando:

Si estás usando Git Shell instalado con GitHub Desktop, el ssh-agent se debe estar ejecutando.
Si estás usando otra indicación, como Git para Windows, puedes usar las instrucciones de "Autolanzamiento del ssh-agent" en Uso de contraseñas para claves SSH" o iníciala manualmente.

# start the ssh-agent in the background
$ eval $(ssh-agent -s)
> Agent pid 59566
Agrega tu llave privada SSH al ssh-agent. Si has creado tu llave con un nombre diferente, o si estás agregando una llave existente que tiene un nombre diferente, reemplaza id_rsa en el comando con el nombre de tu archivo de llave privada.

$ ssh-add ~/.ssh/id_rsa
Agrega la clave SSH a tu cuenta de GitHub

Start the ssh-agent in the background.

$ eval "$(ssh-agent -s)"
> Agent pid 59566
Agrega tu llave privada SSH al ssh-agent. Si has creado tu llave con un nombre diferente, o si estás agregando una llave existente que tiene un nombre diferente, reemplaza id_rsa en el comando con el nombre de tu archivo de llave privada.

$ ssh-add ~/.ssh/id_rsa
Agrega la clave SSH a tu cuenta de GitHub
