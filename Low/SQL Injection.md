# SQL Injection

## Descripción del reto

SQL Injection, trata de explotar vulnerabilidad de formularios mal protegidos mediante consultas SQL.

## Explotación de la vulnerabilidad

1. Para explotar esta vulnerabilidad vamos a introducir los siguientes parametros en el formulario.


```sql
' OR 1=1#
```

![SQLI](/img/SQLI/Captura1.png)

Lo que nos muestra todos los usuarios disponibles en el sistema.