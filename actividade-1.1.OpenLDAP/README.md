# OpenLDAP

## Adrian Francisco Lobato


## Actividade 1.1 - OpenLDAP dende o intérprete de comandos

### 1.Introducción y Preparación del Entorno.

```
1 Configura o enderezo IP do segundo adaptador (en modo Rede Interna). Para iso, edita o
ficheiro de configuración de rede segundo o sistema que uses.
```
![img](img/1.png)
![img](img/2.png)


Primer Adaptador en Nat y el segundo en Red Interna
![img](img/3.png)

Se hacen Ping todo correcto
![img](img/4.png)

### 2.Configuración del Servidor DHCP.

1. Configuración del DHCP.
Primero, configuraremos el servidor DHCP accediendo al archivo de configuración .conf.
Al final de este archivo, realizaremos las modificaciones necesarias.

![img](img/5.png)
```
Después de aplicar los cambios, verificaremos que la configuración es correcta utilizando un
comando específico.
```
```
A continuación, editaremos otro archivo de configuración para especificar qué tarjeta de red
utilizará el DHCP.
```
![img](img/6.png)
```
Finalmente, reiniciaremos el servicio para que los cambios surtan efecto y comprobaremos
su estado.
```
![img](img/7.png)
Una vez hecho esto, conectaremos ambas máquinas a la red interna y confirmaremos que el
cliente ha recibido correctamente una dirección IP.
![img](img/8.png)

### 3.Instalación y configuración de LDAP.

1. Configuración del DHCP.
Instalamos el servicio Ldap-utils
![img](img/9.png)

```
Después ala hora de la instalación seguiremos los siguientes pasos
```
![img](img/10.png)
![img](img/11.png)
![img](img/12.png)
![img](img/13.png)
![img](img/14.png)




### 4.Creación de la unidad organizativa.

1. Crear OU.
Procedemos a generar el archivo necesario para la creación de la unidad organizativa.
![img](img/16.png)
```
A continuación, importamos este archivo al servidor LDAP.
```
![img](img/17.png)
1. Crear usuario.

El proceso para crear usuarios será similar al de los grupos. La única diferencia estará en la
sintaxis del archivo utilizado.

![img](img/18.png)
![img](img/19.png)

