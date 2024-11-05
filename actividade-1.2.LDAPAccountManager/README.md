# Actividade 1.2 - LDAP Account Manager e phpLDAPAdmin

## Instalación de Paquetes

Instalamos los paquetes que necesitamos para hacer la práctica.

![img](img/1.png)

Ver la versión de PHP.

![img](img/2.png)

Sabiendo la versión ya podemos hacer el siguiente comando.

![img](img/3.png)

Reiniciamos el servidor apache2.

![img](img/4.png)

Instalamos el LDAP Account Manager.

![img](img/5.png)

Después de completar la instalación, editamos el siguiente archivo.

![img](img/6.png)

Cambié el adaptador 1 de NAT a Bridge y accedí desde mi PC. Al ingresar la IP del servidor seguida de `/lam` en la barra de direcciones, entramos a **Edit General Settings** y escribimos la contraseña maestra `"lam"`. Luego, cambiamos la contraseña por `"abc123"`.

![img](img/7.png)

En esta opción cambia el idioma a español.

![img](img/8.png)

En la configuración cambiamos al idioma español y ponemos nuestro nombre de dominio.

![img](img/9.png)

En tipos de cuentas pondremos los datos de nuestro dominio.

## Borrar infraestructura

Eliminamos usuarios y grupos.

![img](img/10.png)

## Crear UO, Usuarios y Grupos

### Creación UO

Borramos la UO que teníamos creada.

![img](img/11.png)

Debemos ir a la esquina superior derecha y seleccionar **Herramientas – Unidades Organizativas** para eliminar la UO que ya estaba creada.

![img](img/12.png)

Luego, regresamos al servidor y editamos el archivo `ou.ldif` que creamos en la tarea anterior.

![img](img/13.png)

Para añadir la unidad organizativa, ejecutamos el siguiente comando:

![img](img/14.png)

Crearemos la unidad organizativa llamada "asir".

![img](img/15.png)

### Creación de Grupos

Ahora creamos los grupos en **cuentas/grupos**.

- Profesores Asir
- Profesores Smr

![img](img/16.png)

### Creación de Usuarios

Creamos los usuarios Fabián, Paulo, Alexis en **cuentas/usuario**.

![img](img/17.png)

## Permisos

Pondremos que el grupo "profesoresAsir" tenga permisos de administrador en el archivo `/etc/sudoers`.

![img](img/18.png)

## phpLDAPAdmin

### Instalación y Configuración de PhpLdapAdmin

Instalamos `phpldapadmin`.

![img](img/19.png)

Entramos en `http://192.168.18.139/phpldapadmin/`.

![img](img/20.png)

Configuramos el archivo `/etc/phpldapadmin/config.php`.

![img](img/21.png)

Hacemos clic en **Conectar**, ingresamos el nombre del servidor y el dominio (por ejemplo, local), y luego introducimos la contraseña.

![img](img/22.png)

### Crear UO

Crearemos una UO en **Crear nuevo objeto/Genérico: unidad organizacional** y creamos Clases.

![img](img/23.png)

### Crear Grupo

Crearemos los grupos en **Crear un objeto hijo/Genérico: grupo posix** y crearemos 3 grupos: `clase1`, `clase2`, `clase3`.

![img](img/24.png)

### Crear Usuario

Para agregar usuarios, seguimos el mismo procedimiento: seleccionamos el grupo correspondiente, hacemos clic en **Crear un objeto hijo** y luego elegimos **Genérico: Cuenta de usuario**. En este caso, crearemos a Lucía en el grupo 1, a Manuel en el grupo 2 y a Hugo en el grupo 3.

![img](img/25.png)

Luego deberíamos obtener esta estructura.

![img](img/26.png)

Por último, borramos toda la estructura creada en el punto 4.

![img](img/27.png)

---

**Resumen de la Actividad:**

- Instalación de Paquetes
- Borrar infraestructura
- Crear UO, Usuarios y Grupos
  - Creación UO
  - Creación de Grupos
  - Creación de Usuarios
- Permisos

### phpLDAPAdmin

- Instalación y Configuración de PhpLdapAdmin
- Crear UO
- Crear Grupos y Usuarios

![img](img/28.png)
![img](img/29.png)
