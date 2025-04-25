# XSS Reflected

## Descripción del reto

En este caso estamos delante de un formulario sin proteción contra ejecución de comandos.

## Explotación de la vulnerabilidad

1. Para explotar la vulnerabilidad vamos a introducir el mismo script que en XSS (DOM) pero en el formulario.

```bash
<script>alert("Test")</script>
```

![XSS(Reflected)](/img/XSS(Reflected)/Captura1.png)

2. Y al enviarlo con el boton de Submit vemos que todo a salido correctamente y podemos observar el alert.

![XSS(Reflected)](/img/XSS(Reflected)/Captura2.png)