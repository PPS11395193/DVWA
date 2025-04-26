# SQL Injection

## Descripción del reto

En el nivel medio de SQL Injection vamos a tener que interceptar la peticion con Burpsuit ya que solo disponemos de un menu desplegable.

![SQLI](/img/SQLI/Captura0Medium.jpg)


## Explotación de la vulnerabilidad

1. Interceptamos con Burpsuit la petición.

![SQLI](/img/SQLI/Captura1Medium.jpg)

2. Enviamos la peticion al repeater y modificamos los ultimos parametros por 

```sql
id=1 UNION SELECT user, password FROM users #Submit=Submit
```

![SQLI](/img/SQLI/Captura2Medium.jpg)

3. Y lo enviamos la peticion maliciosas.

![SQLI](/img/SQLI/Captura3Medium.jpg)

Y como podemos ver hemos conseguido explotar correctamente la vulnerabilidad.