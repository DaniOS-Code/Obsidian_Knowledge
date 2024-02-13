> #### Condicionales.
> ``` PowerShell
>$numero = read-host "Escribe un Numero"
>
> $numero = "17"
> if ($numero -eq "1"){
> write-output "Son Iguales"
> } else {
> write-output "Son Distintos"
> }
> ```
> ![[Condicionales-numeros-si-no.png]]

<br>
---
<br>

> #### Otra Forma Podría Ser.
> ``` PowerShell
> $valor = "Hola"
> if ($valor -eq "Hola"){
> write-output "Es Igual a Hola"
> } elseif ($valor -eq "Adios"){
> write-output "Es Igual a Adios"
> } else {
> write-output "No es Hola ni Adios"
> }
> ```
> ![[condicionales-hola-adios.png]]