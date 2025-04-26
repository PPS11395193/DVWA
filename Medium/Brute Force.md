# Fuerza Bruta

## Descripción del reto

En el nivel medio de Brute Force, el unico cambio que tenemos es que entre intentos fallidos hay un retardo de dos segundo. Por lo tanto el metodo del ataque no se va a cambiar.

## Explotación de la vulnerabilidad

1. En primer lugar vamos a ver el codigo fuente del formulario y como envia los datos. Como se puede ver se ultiliza el metodo GET lo cual lo hace vulnerable a ataques por la URL.

![brute force](/img/FuerzaBruta/Captura1.png)

![brute force](/img/FuerzaBruta/Captura2.png)

2. Para explotar esta vulnerabilidad ultilizaremos la famosa herramienta Hydra junto con el dicionario de rockyou. Vamos a suponer que por defecto trataremos conseguir la contraseña del usuario admin. Por lo tanto el comando que vamos a ultilizar es el siguiente. Podemos destacar que -t 30 son los procesos del ataque que se ejecutan al mismo tiempo. Por lo tanto sera bastante rapido.

```bash
hydra -l admin -P /usr/share/wordlist/rockyo.txt 127.0.0.1 http-get-form "/DVWA/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login :F=Username and/or password incorrect." -t 30 
```

Los resultados nos muestran 30 contraseñas diferentes validas. Eso pasa por que estamos ejecutando el ataque sin autentificación en la pagina. Por lo tanto por defecto se aplica la fuerza bruta contra el formulario principal de /dvwa/login.php

![brute force](/img/FuerzaBruta/Captura3.png)

3. Para corregir esto vamos a interceptar la cookie de sesion con Burpsuit llamada PHPSESSID.

![brute force](/img/FuerzaBruta/Captura4.png)

4. Y ahora ejecutaremos el ataque junto con la cookie que hemos interceptado.

```bash
hydra -l admin -P /usr/share/wordlist/rockyo.txt 127.0.0.1 -http-get-form "/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie:PHPSESSID=97dbe3a98a7dfbe5ae407d0cbcb8c904; security=low:F=Username and/or password incorrect." -t 30
```

Y ahora podemos ver el resultado correcto, que nos indica que la contraseña correcta es password.

![brute force](/img/FuerzaBruta/Captura5.png)