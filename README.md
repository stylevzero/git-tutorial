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

Dentro de la información que nos brinda este comando, nos indica sobre que rama estamos parados, en nuestro caso aún no hemos realizado ningún commit y que tenemos archivos que no han sido trackeados, esto último quiere decir que hay archivos que aún no han sido agregados a nuestra staging área. A continuación mediante el siguiente comando agregaremos uno o varios archivos a nuetra staging área.

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

### Guardando nuestro cambios

Si quisieramos guardar cambios de forma local, deberíanos ejecutar el siguiente comando


```
git commit -m "Un breve comentario que describa nuestro commit"
```

Para ver todos los commits que hemos realizados en el repositorio, ejectuamos el siguiente comando


```
git log
```

Si quisieramos acceder a un determinado commit, podríamos hacerlo 

```
git checkout "id del commit"
```

A nivel concepto, cuando hacemos un git log, el Head y el Master no son lo mismo, el Head es el status actual de nuestro proyecto, es decir a donde hicimos el ultimo checkout y el master es el último commit elaborado.

### Hacer un Reset

Podemos decir que son saltos como los checkout pero que borran.

Ejemplo, borra los commits posteriores al que le indiquemos, osea lo que se hiceron después del commit al que quremos ir. Pero conserva los archivos de nuestro directorio de trabajo.

```
git reset --soft "id de commit"
```

En el siguiente ejemplo, borra los commits posteriores al que le indiquemos, osea lo que se hiceron después del commit al que quremos ir y también los archivos de nuestro directorio de trabajo.

```
git reset --hard "id de commit"
```

