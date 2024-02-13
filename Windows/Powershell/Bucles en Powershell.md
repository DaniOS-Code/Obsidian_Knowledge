> #### Bucles `for`.
>
> ```PowerShell
> $frutas = "Manzana", "Banana", "Naranja", "Pera", "Melón"
>
> for ($i = 0; $i -lt $frutas.Count; $i++) {
>     Write-Host $frutas[$i]
> }
> ```
>
> ![[Bucles en Powershell.png]]

<br>
---
<br>

> #### También Podemos Recorrer todos los Elementos de un Documento de Texto.
>
> ```PowerShell
> $archivo = Get-Content "direcciones_ip.txt"
>
> for ($i = 0; $i -lt $archivo.Count; $i++) {
>     Write-Host $archivo[$i]
> }
> ```
>
> ![[recorrer-elementos-document.png]]