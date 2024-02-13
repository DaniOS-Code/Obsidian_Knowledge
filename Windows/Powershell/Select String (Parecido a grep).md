> #### Buscar el Proceso.
> ``` PowerShell
> get-process | select-string lghub
> ```
> ![[get-proceso-system.png]]

<br>
---
<br>

> #### Otra Forma.
> ``` PowerShell
> $variable = 'ping www.google.com'
> invoke-expression $variable | select-string TTL=1*
> ```
> ![[probar-host-ping-grep.png]]