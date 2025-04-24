# Fuerza Bruta

## Descripción del reto

Nuestro objetivo en este ataque es cambiar la contraseña del usuario sin que el usuario se de cuenta.

## Explotación de la vulnerabilidad

Observando el formulario podemos ver que no nos pide ninguna confirmación especial asi como la verificación de la contraseña anterior del usuario. Y ademas el metodo ultilizado es GET lo cual lo hace mas vulnerable aun.

![CSRF](/img/CSRF/Captura1.png)

Para exlotar esta vulnerabilidad simplemente vamos aultiliza la url con la nueva contraseña que queremos ultilizar.

```url
http:/dvwa/dvwa/vulnerabilities/csrf/?password_new=123456&password_conf=123456&Change=Change#
```

![CSRF](/img/CSRF/Captura2.png)
