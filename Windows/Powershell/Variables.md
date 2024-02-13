Las variables son cadenas que contienen información acerca del entorno para el sistema y el usuario que ha iniciado sesión en ese momento

> Crear una Variable.
> ``` PowerShell
> $varible = "Hola"
> $varible
> ```
> ![[Variables-faciles.png]]

<br>
---
<br>

> Guardar la Ejecución de un Comando en una  Variable
> ``` PowerShell
> $variable = 'ping www.google.com'
> Invoke-Expression $variable
> ```
> ![[ping-a-google-datos.png]]