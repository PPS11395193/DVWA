# XSS DOM

## Descripción del reto

Esta prueba es muy parecida al modo low. Viendo el código fuente, el programador solo comprueba si la URL contiene una cadena concreta. Como en el ejercicio anterior no conseguí ejecutar el script, supongo que ahora tampoco funcionarán las soluciones que he visto por Internet.

## Explotación de la vulnerabilidad

1. La opción que deberiamos ultilizar aqui es la siguiente:


```url
</option></select><img src='http://192.168.1.149:9999/a.js'>
```

Lo cual nos pasaria una imagen como una opción valida. Ya que esto esta permitido en el formulario.

![XSS(DOM)](/img/XSS(DOM)/Captura1Medium.jpg)