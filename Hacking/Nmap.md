# Nmap: Herramienta de Escaneo de Redes y Evaluación de Seguridad

[Nmap](https://nmap.org/download.html) es una herramienta versátil utilizada para el escaneo de redes, descubrimiento de hosts, mapeo de redes, análisis de tráfico y evaluación de la seguridad del sistema.

## Escaneos Básicos de Nmap

> Realizar un escaneo de Ping en una red específica:
> ```Bash
> nmap -sP 127.0.0.1/24
> 
> 
> ```
> ![Escaneo de Ping](IPNMAP-ver.png)

<br>
---
<br>

> Escaneo básico de Nmap:
> ```Bash
> nmap 127.0.0.1
> 
> 
> ```
> ![Escaneo Básico](nmap-ez.png)

<br>
---
<br>

> Escanear dos direcciones IP:
> ```Bash
> nmap 127.0.0.1 127.0.0.1
> 
> 
> ```
> ![Escaneo de Dos IPs](nmap-ez-2.png)

<br>
---
<br>

> Escanear todo el rango de una red:
> ```Bash
> nmap 127.0.0.1/24
> 
> 
> ```
> ![Escaneo de Rango de Red](nmap-scan-ez.png)

<br>
---
<br>

> Enumerar un rango de puertos:
> ```Bash
> nmap -p- 127.0.0.1
> 
> 
> ```
> ![Enumeración de Rango de Puertos](nmap-scan-ez2.png)

<br>
---
<br>

> Enumerar todos los puertos:
> ```Bash
> nmap -p- 127.0.0.1
> 
> 
> ```
> ![Enumeración de Todos los Puertos](nmap-ez-3.png)

<br>
---
<br>

> Analizar un rango específico de puertos:
> ```Bash
> nmap -p1-100 127.0.0.1
> 
> 
> ```
> ![Análisis de Rango de Puertos Específico](nmap-ez-4.png)

<br>
---
<br>

> Enumerar los puertos comunes principales (por ejemplo, 500 o 100):
> ```Bash
> nmap --top-ports 100 127.0.0.1
> 
> 
> ```
> ![Enumeración de Puertos Comunes Principales](nmap-ez-5.png)

<br>
---
<br>

> Escaneos UDP con Nmap:
> ```Bash
> sudo nmap -sU --top-ports 100 --open -T5 -v -n 127.0.0.1
> 
> 
> ```
> ![Escaneo UDP](nmap-ez-6.png)

<br>
---
<br>

> Detectar dispositivos conectados en tu red utilizando Ping:
> ```Bash
> nmap -sP 127.0.0.1/24
> 
> 
> ```
> ![Dispositivos Conectados](nmap-sP.png)

<br>
---
<br>

> Detectar dispositivos encendidos en tu red:
> ```Bash
> nmap -sn 127.0.0.1
> 
> 
> ```
> ![Dispositivos Encendidos](nmap-sn.png)

<br>
---
<br>

> Escaneo sigiloso sin dejar rastro en la máquina objetivo:
> ```Bash
> nmap -sS 127.0.0.1
> 
> 
> ```
> ![Escaneo Sigiloso](nmap-sS.png)

<br>
---
<br>

> Aplicar una plantilla para acelerar o ralentizar los escaneos:
> ```Bash
> nmap -T5 127.0.0.1
> 
> 
> ```
> ![Plantilla de Escaneo](nmap-T5.png)

<br>
---
<br>

> Sondeo TCP ACK para identificar el tipo de firewall:
> ```Bash
> nmap -n -v -sA 127.0.0.1
> 
> 
> ```
> ![Sondeo TCP ACK](nmap-cmpljo.png)

<br>
---
<br>

> Scripts de Nmap para obtener información de las máquinas objetivo:
> ```Bash
> nmap --script default 127.0.0.1/24
> 
> 
> ```
> ![Scripts de Nmap](nmap-script.png)

<br>
---
<br>

> Cambiar la dirección MAC:
> ```Bash
> nmap -spoof-mac 12:70:01:00:00:11 127.0.0.1
> 
> 
> ```
> ![Cambiar la Dirección MAC](nmap-mac.png)

<br>

<br>

## Escaneos Avanzados de Nmap

> Escaneo de Nmap más rápido y eficiente:
> ```Bash
> nmap -p- --open -sS -sC -sV --min-rate 5000 -vvv -n -Pn 127.0.0.1 -oN escaneo
> 
> 
> ```
> ![Escaneo Avanzado](nmap-scan-fast.png)

<br>
---
<br>

> Fuzzing con un script de Nmap:
> ```Bash
> nmap --script http-enum -p80 127.0.0.1 -vvv
> 
> 
> ```
> ![Fuzzing](nmap-script2.png)

<br>
---
<br>

> Detectar vulnerabilidades:
> ```Bash
> nmap --script vuln -p 127.0.0.1
> 
> 
> ```
> ![Detección de Vulnerabilidades](nmap-script3.png)

<br>
---
<br>

Utilizar Metasploit para explotar vulnerabilidades y obtener acceso al sistema:
![Explotación con Metasploit](nmap-metasploit.png)

Configuraciones básicas:
![Configuración Básica](nmap-config-meta.png)

Configurar el payload correspondiente:
![Configuración del Payload](nmap-payload.png)

Ejecutar el comando "Run" para obtener acceso:
![Ejecutar Comando "Run"](nmap-payload-run.png)

<br>
---
<br>

> Ataques de fuerza bruta SSH:
> ```Bash
> nmap --script ssh-brute 127.0.0.1
> 
> 
> ```
> ![Ataques de Fuerza Bruta SSH](FBruta-ssh.png)

<br>
---
<br>

> Probar diferentes contraseñas para un usuario:
> ```Bash
> nmap -p 22 --script ssh-brute --script-args userdb='usuario.txt',passdb='rockyou.txt' 127.0.0.1
> 
> ```
> ![Pruebas de Contraseñas](confirm-contr-ssh.png)