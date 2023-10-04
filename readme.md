# Paquete DEB uab-wireshark-common
Paquete que pre-configura el wireshark-common para que se puede ejecutar desde 
usuarios no privilegiados

# Generar el esqueleto inicial


```
DEBFULLNAME="Jordi Román Mejias" dh_make --email Jordi.Roman@uab.cat -i -c gpl3 --native -p uab-wireshark-common_1.0
```

# Como Crear el paquete DEB a partir del codigo de GitHub
Para crear el paquete DEB será necesario encontrarse dentro del directorio donde 
localizan los directorios que componen el paquete.  Una vez allí, se ejecutará el 
siguiente comando (es necesario tener instalados los paquetes apt-get install 
debhelper devscripts):

```
apt-get install debhelper devscripts
/usr/bin/debuild --no-tgz-check -us -uc
```

# Como Instalar el paquete generado *.deb:
Para la instalación de paquetes que estan en el equipo local puede hacerse uso de
 ***dpkg*** o de ***gdebi***, siendo este último el más aconsejado para que se 
instalen también las dependencias correspondientes.

```
gdebi -i *.deb
```
