# Practica docker nginx
## Descargar imagen

Primero de todo descargaremos la imagen de nginx de la [página oficial de docker](https://hub.docker.com/_/nginx).

![](https://i.imgur.com/VyryX5c.png)

Copiaremos el comando que aparece en la página y lo ejecutaremos en la terminal.

```bash
$ docker pull nginx
```

![](https://i.imgur.com/ir5XJNG.png)

En mi caso, como yo ya lo he descargado previamente, me dice que la imagen está actualizada a la ultima versión.

## Ejecutar la imagen
```bash
$ docker run --rm -d -p 8080:80 --name web nginx
```

Usando el comando anterior, ejecutaremos la imagen con diferentes parametros:
-  `--rm`: Borra automaticamente cuando sale del contenedor
-  `-d`: MODO DEMONIO, el contenedor se ejecuta en segundo plano y solo se muestra su ID
-  `-p`: Especificas el puerto del host
-  `--name`: Asignas un nombre al contenedor
-  Por ultimo indicamos la imagen que queremos ejecutar

![](https://i.imgur.com/fwrNMAB.png)

Una vez ejecutado la instrucción prodremos ir a la dirrecion `localhost:8080` y veremos la página por defecto de Nginx.

![](https://i.imgur.com/dwYq77L.png)

Despues, para cerrar el contenedor utilizaremos el siguiente comando especificando el nombre del contenedor que queremos cerrar.
```bash
$ docker stop web
```

## Ejecutar la imagen cambiando el documento por defecto
 Por defecto nginx busca
 
