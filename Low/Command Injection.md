# Command Injection

## Descripción del reto

En esta vulnerabilidad se permite introducir comandos de consola dentro de un formulario.

## Explotación de la vulnerabilidad

1. Para esta vulnerabilidad vanos a intentar introducir el comando whoami despues de introducir una ip separado por un ;

```bash
127.0.0.1; whoami
```

![Command Injection](/img/CommandInjection/Captura1.png)

Con esto podemos ver que el usuario acual en el que nos encontramos es www-data.