cambiahostname
==============

Script que permite cambiar el nombre de host de un equipo y realizar un pkgsync tras cambiarlo   

Esteban M. Navas <algodelinux@gmail.com>   
Fecha creación:      08/07/2016   
Última modificación: 12/06/2018   

Instalación
-----------

La forma más sencilla de instalarlo es ejecutar los siguientes comandos:

   wget --no-check-certificate -O /usr/local/sbin/cambiahostname https://raw.githubusercontent.com/algodelinux/cambiahostname/master/cambiahostname  
   chmod 755 /usr/local/sbin/cambiahostname  
  

Uso                   
---

* Es posible introducir el nombre de la máquina como parámetro.   
* Si no se introduce el nombre como parámetro, tratará de obtenerlo consultando al DNS definido en DNSSERVER.   
* Si no se puede obtener el nombre consultando al servidor DNS, se solicita su introdución mediante teclado.   
