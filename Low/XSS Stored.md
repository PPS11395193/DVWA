# XSS Stored

## Descripción del reto

En este caso estamos delante de un formulario con mas campos sin proteción contra ejecución de comandos, tenemos una diferencia importante y es que el primer campo esta protegido a un maximo de 10 caractares y el segundo a 50. Por lo tanto el objetivo sera el segundo campo.

## Explotación de la vulnerabilidad

1. Para explotar la vulnerabilidad vamos a introducir el mismo script que en XSS pero en el segundo campo del formulario.

```bash
<script>alert("Test")</script>
```

![XSS(Stored)](/img/XSS(Stored)/Captura2.png)

2. Y al enviarlo con el boton de Sign Guestbook vemos que todo a salido correctamente y podemos observar el alert.

![XSS(Stored)](/img/XSS(Stored)/Captura3.png)