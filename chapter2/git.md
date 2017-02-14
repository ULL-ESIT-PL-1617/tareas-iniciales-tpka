#Git

[Git](https://git-scm.com/) se trata de un sistema de control de versiones gratuito y de código abierto que permite desarrollar proyectos de manera rápida y eficiente.
El control de versiones se puede llevar a cabo de manera local, centralizada o distribuida. 

![](https://git-scm.com/book/en/v2/images/distributed.png)

* La comunicación entre estos nodos se debe llevar a cabo de manera segura y automatizada, por ello desde cada máquina local, deberemos hacer uso de un cifrado simétrico. Por lo tanto, deberemos generar una clave pública desde nuestra máquina local y establecer dicha conexión. El procedimiento es el siguiente:

    1. Ejecutar ssh-keygen -t dsa en la máquina local para generar dos ficheros: ~/.ssh/id_dsa.pub (clave pública) y~/.ssh/id_dsa (clave privada).
    2. A continuación deberemos crear el fichero ~/.ssh/config, con el siguiente contenido PubkeyAcceptedKeyTypes +ssh-dss.
    3. Por último, copiar el contenido del fichero ~/.ssh/id_dsa.pub en el apartado Settings -> SSH and GPG keys -> Add SSH key de nuestro perfil en Github desde un navegador, dar un título a esa conexión y confirmar.
    
Antes de empezar a trabajar en nuestros proyectos, deberemos configurar nuestro usuario global de git y otros datos. Una vez llevado a cabo, para crear un repositorio, simplemente ejecutar ***git init*** en cualquier directorio que hallamos creado explicitamente para esta tarea.
