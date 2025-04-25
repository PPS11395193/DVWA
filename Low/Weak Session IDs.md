# Weak Session IDs

## Descripción del reto

En este reto vamos a intercepar las cookies y intentaremos cambiar el id generado.

## Explotación de la vulnerabilidad

1. Para explotar esta vulnerabilidad vamos a intercepar la petición con burpsuit para recibir las cookie, despues de generarla en la pagina web.

![weaksessionsID](/img/weaksessionsID/Captura1.png)

![weaksessionsID](/img/weaksessionsID/Captura2.png)

2. Como se puede ver en la primera captura el calor de la cookie es 1. Pero al interceptarlo con el burpsuit lo enviamos al repeater y modificamos el valor a 2. Con esto lo enviamos y al observar otra vez el valor de la cookie en la web podemos ver que se ha cambiado al 2.

![weaksessionsID](/img/weaksessionsID/Captura3.png)
