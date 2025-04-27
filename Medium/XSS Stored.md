# XSS Stored

## Descripción del reto

En este nivel medio se ha protegido el campo de Message por lo tanto ya no lo podemos explotar como antes. Para este caso vamos a interceptar la petición con burpsuit.

## Explotación de la vulnerabilidad

1. Una vez interceptado la petición vamos a poner el script en el campo de Name ya que este campo solo esta protegido con un maximo de 10 caracteres en el lado del cliente.

```bash
<script>alert("Test")</script>
```

![XSS(Stored)](/img/XSS(Stored)/Captura1Medium.jpg)

2. Y al enviarlo con Burpsuit, y recargar la pagina ya podremos ver la salida del alert.

![XSS(Stored)](/img/XSS(Stored)/Captura2Medium.jpg)