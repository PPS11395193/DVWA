# CSRF

## Descripción del reto

En este caso la protecion del nivel medio es que el servidor comprueba si la solicitud se ha realizado desde un servidor legitimo.

## Explotación de la vulnerabilidad

1. Vamos a interceptar la peticion con Burpsuit y enviarl la respuesta en el repiter.

![CSRF](/img/CSRF/Captura1Medium.jpg)

Y con esto podremos cambiar la contraseña correctamente.