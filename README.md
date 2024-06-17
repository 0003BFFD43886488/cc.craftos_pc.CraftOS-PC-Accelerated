# Servidor MariaDB
Este paquete contiene una serie de archivos .rpm que juntos componen la distribución de MariaDB Server.

 Los paquetes incluidos en este archivo pueden variar según el sistema operativo que esté utilizando y su versión, ya que diferentes componentes pueden requerir bibliotecas o funcionalidades disponibles solo en versiones más recientes.

 Los archivos .rpm se pueden instalar individualmente, pero existen interdependencias complejas que son difíciles de resolver utilizando rpm únicamente.  Por esa razón, este paquete se distribuye como un archivo Yum listo para usar, de modo que pueda usar yum para instalar los paquetes que contiene.

 Para que el administrador de paquetes pueda instalar estos paquetes, deberá colocarlos en una ubicación a la que el administrador de paquetes tenga privilegios de acceso.  Es posible que /opt sea una buena ubicación donde descomprimir el archivo y el administrador de paquetes podrá leerlo.

 Para usar el archivo con yum, cree un archivo mariadb.repo en `/etc/yum.repos.d/` que apunte al directorio donde extrajo los archivos.  En este archivo se incluye un script útil llamado `setup_repository` para hacer esto por usted.

 Deberá realizar este trabajo como root para poder escribir archivos en estas ubicaciones.

```
 cd /opt tar -xf ~/mariadb-11.2.2-rhel-7-x86_64-rpms.tar mariadb-11.2.2-rhel-7-x86_64-rpms/setup_repository
```

 Una vez configurado el repositorio, debe instalar el paquete del servidor MariaDB.

 `yum instalar -y servidor MariaDB`

 Para obtener más información sobre la instalación de archivos .rpm de MariaDB, visite: https://mariadb.com/kb/en/installing-mariadb-rpm-files/

 Para obtener más información sobre los productos MariaDB, visite https://mariadb.com/products y para obtener ayuda con el uso de MariaDB, comuníquese con MariaDB Corporation: https://mariadb.com/contact
