SQL ORACLE DEVELOPER

Para la instalación de Oracle SQEL Developer es necesario descargar desde la siguiente URL:

[http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html)  
Dentro de la pagina tenemos que aceptar los terminos y condiciones para la descarga que se muestra en la parte de arriba, despues de esto debemos seleccionar el archivo a descargar en este caso para esta instalacion nos iremos a la opcion "Other Platforms" el cual nos descargara un fichero ".zip"  
![](/pictures/OracleSQLDownload.png)

Oracle nos pide crear o logearnos con una cuenta dentro de su portal, por lo tanto se observara una ventana como la siguiente, en la cual debemos introducir nuestras credenciales o bien crear una cuenta la cual no nos toma mas de un minuto en su creación, esto con el fin de otorgarnos el permiso para descarga.

![](/pictures/loginoracle.png)

Podremos ver la descarga completa o el progreso de la misma dependiendo el explorador que estemos utilizando.  
![](/pictures/FIcheroSQLDeveloper.png)

Dentro del directorio en el que se descargo nuestro fichero .zip procedemos a la instalación por medio de los siguientes comandos:  
Para desempaquetar nuestro archivo dentro de la carpeta /opt:

```
sudo unzip sqldeveloper-17.2.0.188.1159-no-jre.zip -d /opt
```

Despues validamos que se haya creado el directorio /sqldeveloper moviendonos a dicho directorio:

```
cd /opt/sqldeveloper
```

Dentro de nuestra carpeta editamos el archivo sqldeveloper.sh para configuración:

```
gedit sqldeveloper.sh
```

Nos abrira nuestro editor de texto en este caso 'gedit', vamos a alterar el contenido de este archivo comentando las primeras dos lineas y pegando las ultimas dos nuevas lineas como se muestra a continuación:

    #!/bin/bash
    #cd “`dirname $0`”/sqldeveloper/bin && bash sqldeveloper $*

    export JAVA_HOME=/usr/lib/jvm/java-8-oracle/
    cd /opt/sqldeveloper/sqldeveloper/bin && bash sqldeveloper $* &

* NOTA: Nuestro paquete descargado desde la pagina anteriormente mencionada ya incluye el SDK Java 8 por lo tanto no hay que realizar nada en cuestion a la version Java.

Guardamos y ceramos nuestro archivo sqldeveloper.sh y procemos a crear un link simbolico:

```
sudo ln -s /opt/sqldeveloper/sqldeveloper.sh /usr/local/bin/sqldeveloper
```

Ahora podemos correr el comando sqldeveloper y nos abrira la interfaz de nuestra aplicacion.![](/pictures/interfazsqloracle.png)

