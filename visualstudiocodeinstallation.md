Instalación de Visual Studio Code

Visual Studio Code es un editor de código fuente desarrollado por Microsoft para Windows , Linux y macOS . Incluye soporte para depuración , control Git incorporado , resaltado de sintaxis , finalización de código inteligente , fragmentos y refactorización de código . También es personalizable, por lo que los usuarios pueden cambiar el tema del editor , atajos de teclado y preferencias. Es libre y de código abierto y su descarga para la distribución de Ubuntu se lleva a cabo por medio de la página principal de Visual Studio code.

[https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)

En la cual debemos elegir la opción necesaria, en este caso descargamos el fichero con extención ".deb" para Debian, Ubuntu.

![](/pictures/visualdownload.png)

Ya que hayamos elegido la opción a descargar dependiendo que explorador estamos utilizando veremos el progreso de la descarga.
![](/pictures/visualDownloading.png)

Cabe recordar que los archivos .deb en el siguiente ejemplo dentro de Ubuntu 16.04 se puede instalar directamente al abrir el fichero que resulte de la descarga, la cual nos muestra una ventana de "Software de Ubuntu" en la cual solo es necesario dar click en el boton de instalar para comenzar con la instalación. 
![](/pictures/InstaladorVisual.png)

Antes de proceder el sistema a la instalación hara la petición de las credenciales para autenticar al administrador del equipo.
![](/pictures/CredentialRoot.png)

* Otra opción teniendo el fichero .deb ya descargado (en nuestro caso code_1.16.1-1505406497_amd64 version actual) es realizar la instalación desde la consola con los siguientes comandos:
Desempaquetamos: 
~~~
sudo dpkg -i code_1.16.1-1505406497_amd64.deb
~~~
Instalamos: 
~~~
sudo apt-get install -f
~~~
Despues, al termino de la instalación automatica o por terminal podremos hacer uso de Visual Studio Code, encontrando en las aplicaciones de nuestro sistema la aplicación con dicho nombre.

![](/pictures/visuallink.png)




