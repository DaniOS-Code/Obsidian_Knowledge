# Comados para obtener datos del Sistema

Hay varios Comandos en con `get` que nos sirve para saber cualquier tipo de Información del Sistema.

> #### Para Conocer el HOST.
> ```PowerShell
> get-host
> ```
> ![[Comando Get-.png]]

<br>
---
<br>

> #### Para Conocer el PATH Actual.
> ```PowerShell
> $location = get-location
> ```
> ![[Get-location.png]]

<br>
---
<br>

> #### Para ver los Procesos del Sistema.
> ```PowerShell
> $procesos = get-process
> ```
> ![[Get-procesos.png]]

<br>
---
<br>

> #### Para ver la Fecha Actual.
> ```PowerShell
> $fecha = get-date
> ```
> ![[Get-fecha.png]]

<br>
---
<br>

> #### Para Extraer Información de un Archivo.
> ```PowerShell
> get-content direcciones_ip.txt | Select-String -Pattern "192"
> ```
> ![[Get-informacion-archivo.png]]

