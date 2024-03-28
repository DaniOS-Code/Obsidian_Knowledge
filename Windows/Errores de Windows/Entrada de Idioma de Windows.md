# Remover entrada de idioma del teclado no deseado

Remover las entradas de idiomas del teclado ayuda a que no estorben y se cambien sin querer las entradas de idioma, esto te pueden ayudar bastante cuando por ejemplo no tienes la letra `ñ` pero puedes activarla con los atajos de `ALT-GR` + `n` que te daría la tecla `ñ`

## Como primer paso tenemos que ver la listas de idiomas que tenemos

para poder ver las entradas que tenemos en el Sistema realizaremos el siguiente código:

```PowerShell
get-winuserlanguajelist


```

![[WinError-LengUS.png]]

## Como segundo paso pondremos el mismo código pero al final pondremos el `LanguageTag`

El `languageTag` esta en la parte superior de cada sección (si es que tienes mas de 1 lenguaje en windows), ahora solo tendremos que poner el Tag que en mi caso seria `en-US`

```PowerShell
get-winuserlanguagelist en-US


```

![[WinError-LengUS.png]]
Ahora solo tenemos que escribir `Y` + `Enter` y luego tendremos que ir a Idiomas 

## Últimos pasos

Ahora tendremos que dirigirnos a `region e idioma` en la configuración de windows y luego ir a opciones de lenguaje

![[Language&region.png]]

Ahora tendremos que verificar si lo hemos eliminado correctamente, y si no solo agregaremos otra entrada de idioma y luego lo eliminaremos permanentemente (lo pueden volver a poner no es para siempre es solo para que tengan por defecto el que quieran)

![[optionlanguageUs.png]]