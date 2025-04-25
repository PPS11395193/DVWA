# Weak Session IDs

## Descripción del reto

En el formulario de la web tenemos un menú desplegable con varias opciones de idioma. Al elegir un idioma, la URL cambia y añade al final: default=English (http://dvwa/dvwa/vulnerabilities/xss_d/?default=English). Lo cual nos llega a pensar que cambiando el final de URL no permita introducir comandos.

## Explotación de la vulnerabilidad

1. Añadiremos al final de la URL despues de default=

```bash
<script>alert("Test")</script>
```

2. Y al refrescar la pagina podemos ver que ha funcionado correctamente y nos ha sacado el alert en nuestra pagina.

![XSS(DOM)](/img/XSS(DOM)/Captura1.png)
