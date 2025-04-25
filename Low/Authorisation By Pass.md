# Authorisation By Pass

## Descripción del reto

En este reto debemos de cambiar el nombre de los usuarios con el usuario gordonb que nos indican en la web. Al inicial sesion con el no vemos el reto de Authorisation By Pass.

## Explotación de la vulnerabilidad

1. Para aceder a la pagina de Authorisation By Pass deberemos introducir la ruta URL de este reto.

``` url
http://mi.local/DVWA/vulnerabilities/authbypass
```

![authorisationByPass](/img/authorisationByPass/Captura1.png)

2. Como podemos ver estamos con el usuario correcto. Ahora cambiamos algun nombre y pulsamos en Update. Al refrescar la pagina podemos ver que los cambios se han aplicado correctamente.

![authorisationByPass](/img/authorisationByPass/Captura2.png)
