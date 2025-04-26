# File Upload

## Descripción del reto

La protecion de este nivel es que solo podemos enviar archivos png o jpeg. Por lo tanto deberemos de usar Burpsuit para interceptar el envio del formulario.

![File upload](/img/FileUpload/Captura1Medium.jpg)

## Explotación de la vulnerabilidad

1. Interceptamos la peticion en  burpsuit.

![File upload](/img/FileUpload/Captura2Medium.jpg)

2. Lo enviamos al repiter y cambiamos el Content-Type por image/png

![File upload](/img/FileUpload/Captura3Medium.jpg)

2. Ahora nos pondremos en escucha por el puerto 4444 y esperaremos la respuesta.

```bash
nc -lvnp 4444
```