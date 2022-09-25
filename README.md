# Git tutorial

### Configuración inicial que utilizaremos para indentificarnos
(Desde la línea de comandos - Git Bash)

##### Configuramos el nombre

```
git config --global user.name "Mi nombre"
```

######
Comprobamos que se hayan guardado los cambios

```
git config --global user.name
```

##### Configuramos la dirección de correo

```
git config --global user.email "micasilladecorreo@estoesunaprueba.com"
```

#####
Comprobamos que se hayan guardado los cambios

```
git config --global user.email
```

### Comenzando a trackear los cambios

###### Posicionados en nuestro directorio de trabajo, para inicializar git utilizaremos el  comando:

```
git init
```

###### Si quisieramos chequer el estado de nuestro repositorio

```
git status
```

Dentro de la información que nos brinda, nos indica sabore que rama estamos parados, en nuestor caso aún no hemos realizado ningún commit y que tenemos archivos que no han sido trackeados, esto último quiere decir que hay archivos que aún no han sido agregados a nuestra staging área. A continuación mediante el siguiente comando agregaremos uno o varios archivos a nuetra staging área.

```
git add nombreDelArchivo
```

Si quisieramos agregar todos los archivos a nuestra staging área, deberiamos utilizar el siguiente comando.

```
git add -A
```

Si quisieramos sacar o eliminar  un archivo de nuestra staging área, usariamos el siguiente comando.

```
git rm --cached nombreDelArchivo
```
