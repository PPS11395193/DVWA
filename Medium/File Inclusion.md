# File Inclusion

## Descripción del reto

El nivel medio tiene la protecion de no poder ingresar los ../ y \ los cuales remplaza por espacios en blanco. Pero en mi caso no ultilizo esto y directamente pongo la ruta principal. Por lo tanto no vamos a cambiar nada.

## Explotación de la vulnerabilidad

1. Como podemos observar en este caso se ultiliza la url para abrir los formularios y distintas paginas.

![File inclusion](/img/FileIncludion/Captura1.png)

2. Por lo tanto vamos a intentar aceder direcamente a un archivo privilegiado del sistema como es /etc/passwd.

```url
http://mi.local/DVWA/vulnerabilities/fi/?page=/etc/passwd
```

Como podemos ver el contenido del archivo se muestra en la parte superior de la pagina. Por lo que hemos explotado correctamente la vulnerabilidad.

![File inclusion](/img/FileIncludion/Captura2.png)