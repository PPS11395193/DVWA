# Command Injection

## Descripción del reto

En este nivel de Command Injection medium, hay una minima proteción en el formulario que hace evitar && o ; reemplazándolos con espacios. 

## Explotación de la vulnerabilidad

1. En este caso usaremos el simbolo de | llamado pipa que haca ejecutar los dos comandos.

```bash
127.0.0.1| cat /etc/passwd
```

![Command Injection](/img/CommandInjection/Captura1Medium.jpg)

Y como podemos observar esto ha funcionado correctamente.