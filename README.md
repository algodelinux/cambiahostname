cambiahostname
==============

Script que permite cambiar el nombre de host de un equipo y realizar un pkgsync tras cambiarlo   


Instalación
-----------

La forma más sencilla de instalarlo es ejecutar los siguientes comandos:

   wget --no-check-certificate -O /usr/local/sbin/cambiahostname https://raw.githubusercontent.com/algodelinux/cambiahostname/master/cambiahostname  
   chmod 755 /usr/local/sbin/cambiahostname  
  

Uso
---

* Es posible introducir el nombre de la máquina como parámetro.   
* Si no se introduce el nombre como parámetro, tratará de obtenerlo consultando al DNS definido en DNSSERVER.   
* Si el hostname de la máquina es 'modelo', y no se ha encontrado un hostname para el equipo en el servidor DNS, se utilizará como hostname la dirección MAC de la interfaz de red ethernet.   
* Si no se puede obtener el nombre consultando al servidor DNS, se solicita su introdución mediante teclado.   
  

Sintaxis
--------

```bash
cambiahostname [OPTIONS]

Opciones reconocidas:
        -h               mostrar esta ayuda y salir.
        -n HOSTNAME      introducir el nombre de host. (sólo se cambiará el hostname si no existe una entrada DNS para este HOST)
        -d DNSSERVER     introducir el servidor DNS.
        -s               ejecutar sinc_puppet.
        -p               ejecutar pkgsync.
```
   
   
Ejemplos
--------

```bash
# cambiahostname -h
# cambiahostname a20-pro 
# cambiahostname -n a20-pro 
# cambiahostname -d servidor 
# cambiahostname -n a20-pro -d servidor 
# cambiahostname -sp
# cambiahostname -n a20-pro -s
# cambiahostname -n a20-pro -p 
# cambiahostname -n a20-pro -sp 

```
   
   
Authors
-------

Esteban M. Navas <algodelinux@gmail.com>   
Fecha creación:      08/07/2016   
Última modificación: 07/02/2019   
