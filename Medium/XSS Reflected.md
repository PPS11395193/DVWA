# XSS Reflected

## Descripción del reto

En el nivel medio de XSS Reflected hay un pequeño cambio y es que no podemos introducir:

```
script
```
En nuestro formulario.

![XSS(Reflected)](/img/XSS(Reflected)/Captura0Medium.jpg)


## Explotación de la vulnerabilidad

1. Para explotar la vulnerabilidad vamos a modificar el script en mayusculas para esquivar la proteción.

```bash
<SCRIPT>alert("Test")</SCRIPT>
```

![XSS(Reflected)](/img/XSS(Reflected)/Captura1Medium.jpg)

2. Y al enviarlo con el boton de Submit vemos que todo a salido correctamente y podemos observar el alert.

![XSS(Reflected)](/img/XSS(Reflected)/Captura2Medium.jpg)