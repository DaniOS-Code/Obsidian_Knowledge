> #### Para Eliminar un Archivo.
> ``` PowerShell
> rm ".\Imagen.png"
> ```

---

> #### Para Renombrar un Archivo.
> ``` PowerShell
> ren ".\Expresiones.mp4" ".\Pequeñas Expresiones"
> ```

---

> #### Para Copiar Archivos.
> ``` PowerShell
> copy-item -path ".\Animales.mp4" -destination server
> ```

---

> #### Crear un Directorio.
> ``` PowerShell
> new-item -path "Carpeta" -itemtype directory
> ```

---

> #### Crear un Archivo.
> ``` PowerShell
> new-item -path "Hola.txt" -itemtype file
> ```