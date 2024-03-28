# Saturación de Recursos para Inutilizar un Servicio

Un ataque de denegación de servicio (DoS) es un intento malicioso de abrumar un sistema, servicio o red con un flujo excesivo de tráfico, con el objetivo de que se vuelva inaccesible para usuarios legítimos.

## Paralizar un Servidor Mandando Muchos Paquetes TCP

Para paralizar un servidor enviando muchos paquetes TCP, puedes utilizar la herramienta `hping3`. Este comando genera y envía paquetes de red con las siguientes opciones:

- `--icmp`: Utilizado para enviar mensajes ICMP (Internet Control Message Protocol), como pings y trazas de ruta.
- `--rand-source`: Indica que la dirección IP de origen de los paquetes se seleccionará aleatoriamente.
- `--flood`: Esta opción indica que la herramienta debe enviar paquetes lo más rápido posible, sin esperar respuestas.
- `-d 1400`: Establece el tamaño de datos en los paquetes ICMP en 1400 bytes. ICMP generalmente contiene información de control o mensajes de error.
- `Dirección IP`: La dirección IP de destino a la que se enviarán los paquetes ICMP.

```Bash
hping3 --icmp --rand-source --flood -d 1400 127.0.0.1


```

![Ataque DoS con paquetes ICMP](ataques-DoS.png)

## Otra Forma pero en un Puerto en Concreto

Otra forma de realizar un ataque DoS es dirigirlo a un puerto específico. En este caso, nuevamente utilizamos `hping3` con las siguientes opciones:

- `--rand-source`: Indica que la dirección IP de origen de los paquetes se seleccionará aleatoriamente.
- `-d 500`: Establece el tamaño de datos en los paquetes.
- `Dirección IP`: La dirección IP de destino a la que se enviarán los paquetes.
- `-p 80`: Especifica el puerto de destino en el que se enviarán los paquetes. En este caso, el número 80 representa el puerto utilizado para el protocolo HTTP, que es el protocolo de navegación web.
- `--flood`: Indica que la herramienta debe enviar paquetes lo más rápido posible, sin esperar respuestas.

```sh
hping3 --rand-source -d 500 127.0.0.1 -p 80 --flood


```

![Ataque DoS en un puerto específico](hping3-bytes.png)

![Resultado del ataque en Firefox](DoS-firefox.png)