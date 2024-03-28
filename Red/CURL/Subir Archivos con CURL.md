> #### Por Ejemplo, Si quieres subir un archivo llamado `Imagen.png` a la URL `https://ejemplo.com/subir`.
> ```Bash
> curl -f "file=@/ruta/completa/a/imagen.png"
> https://ejemplo.com/subir
> 
> ```

---

> #### También puedes subir ficheros con `CURL` a través del protocolo FTP.
> ```Bash
> curl -t hola.pdf ftp://192.123.0.10/home/Daniel/ -u Daniel:123123
> 
> 
> ```