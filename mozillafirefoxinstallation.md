Mozilla Firefox version 51.0  
\(Versión para funcionalidad de VPN\)

Para la instalación de nuestro explorador Firefox en su version anterior 51.0 es necesario seguir los siguientes comandos desde tu terminal, cabe mencionar que firefox se instala con la opción de actualización automatica asi que se recomienda que antes de terminar la instalación desconectemos nuestra red \(wifi o ethernet\) esto con el fin de ejecutar la aplicación y hacer lo necesario para desactivar las actualizaciones automaticas como al termino se explica.

Primeramente actualizamos nuestra lista de repositorios del sistema:

```
sudo apt-get update
```

Despues de ello comenzamos la descarga del fichero .tar.bz2 que corresponde a la versión 51.0, esto puede demorar unos minutos:

```
wget https://ftp.mozilla.org/pub/firefox/releases/51.0/linux-x86\_64/en-US/firefox-51.0.tar.bz2
```

Para desempaquetar el fichero:

```
tar -xjf firefox-51.0.tar.bz2
```

Es recomendable mover lo que obtuvimos del desempaquetado a la carpeta /opt/firefox51 con el comando:

```
sudo mv firefox /opt/firefox51
```

* En caso de que el directorio en opt "/firefox51" no se encuentre, crearlo con el comando y mover al nuevo directorio como en el paso anterior.

  ```
  sudo mkdir /opt/firefox51
  ```

* En caso de tener una version de firefox previamente instalada remover dicha version con el comando:

  ```
  sudo rm -rf /opt/firefox55 \(firefox55 o numero de version, para saber que version se tiene ir a la pestaña de "About" en la aplicacion de firefox abierta\).
  ```

  Para crear el link simbolico de la aplicacion es cuestion de correr la siguiente linea:

  ```
  sudo ln -s /opt/firefox51/firefox /usr/bin/firefox
  ```

Despues de los pasos anteriores podemos mandar llamar la aplicacion desde la terminal

```
firefox
```

Podemos validar y confirmar la version de firefox despues de abrir la aplicación en la opcion de "about"

Para desactivar las actualizaciones automaticas podemos seguir los siguientes pasos:

Seleccionamos dentro del menú la opcion de preferencias, la cual nos arrojara la siguiente ventana 
![](/pictures/preferencesfirefox.png)

En la ventana de preferencias nos vamos a la opcion de avanzadas, en la cual seleccionaremos la pestaña de actualizaciones (Update) y marcamos la opcion NUNCA VALIDAR ACTUALIZACIONES. 
![](/pictures/advancepreferencesfirefox.png)

Con esto nuestro firefox no buscara actualizaciones automaticas y se instalaran solo si nosotros buscamos dichas actualizaciones. 
