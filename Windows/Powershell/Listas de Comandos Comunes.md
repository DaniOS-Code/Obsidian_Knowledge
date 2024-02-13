> #### Cambiar el Directorio Actual.
> ```PowerShell
> cd C:\Users\Usuario\Documents
> ```

---

> #### Mostrar el Contenido del Directorio Actual.
> ```PowerShell
> dir
> ```

---

> #### Crear un Nuevo Directorio.
> ```PowerShell
> mkdir NuevaCarpeta
> ```

---

> #### Eliminar un Archivo.
> ```PowerShell
> del archivo.txt
> ```

---

> #### Copiar un Archivo.
> ```PowerShell
> copy archivo1.txt archivo2.txt
> ```

---

> #### Mover un Archivo.
> ```PowerShell
> move archivo.txt C:\Usuarios\Usuario\Documentos
> ```

---

> #### Renombrar un Archivo.
> ```PowerShell
> ren archivo.txt nuevo_nombre.txt
> ```

---

> #### Mostrar el Contenido de un Archivo de Texto.
> ```PowerShell
> type archivo.txt
> ```

---

> #### Mostrar Mensajes en la Pantalla o Redirigir Texto a un Archivo.
> ```PowerShell
> echo Hola, mundo!
> ```

---

> #### Limpiar la Pantalla de la Terminal.
> ```PowerShell
> cls
> ```

---

> #### Limpia la Terminal.
> ```PowerShell
> Clear
> ```

---

> #### Mostrar una lista de Procesos en Ejecución.
> ```PowerShell
tasklist
> ```

---

> #### Finalizar un Proceso.
> ```PowerShell
> taskkill /IM nombre_proceso.exe
> ```

---

> #### Mostrar la Configuración de Red del Equipo.
> ```PowerShell
> ipconfig
> ```

---

> #### Enviar un Paquete de Prueba a una Dirección IP.
> ```PowerShell
> ping google.com
> ```

---

> #### Mostrar la Ruta Tomada por los Paquetes hasta un Destino.
> ```PowerShell
> tracert google.com
> ```

---

> #### Mostrar la Estructura de Directorios en Forma de Árbol.
> ```PowerShell
> tree
> ```

---

> #### Limpiar la Caché DNS del Equipo.
> ```PowerShell
> ipconfig /flushdns
> ```

---

> #### Mostrar Información Detallada sobre la Configuración del Sistema.
> ```PowerShell
> systeminfo
> ```

---

> #### Escanear y Reparar Archivos del Sistema Dañados.
> ```PowerShell
> sfc /scannow
> ```

---

> #### Apagar o Reiniciar el Equipo. Apagar`s`, Reiniciar`r` y Tiempo`t`
> ```PowerShell
> shutdown /s
> shutdown /r
> shutdown /t /r
> ```

---

> #### Abrir la Calculadora de Windows.
> ```PowerShell
> calc
> ```

---

> #### Abrir el Mapa de Caracteres para Copiar Símbolos Especiales.
> ```PowerShell
> charmap
> ```

---

> #### Mostrar o Modificar la Encriptación de Archivos en un Directorio. La Primera para Encriptar y la Segunda para Desencriptar.
> ```PowerShell
> cipher /e C:\Directorio
> cipher /d C:\Directorio
> ```

---

> #### Interfaz de Línea de Comandos para Administrar el Sistema y Obtener Información del Hardware.
> ```PowerShell
> wmic process get Caption,ProcessId,CommandLine
> ```

---

> #### Mostrar Información sobre la Versión de Windows Instalada.
> ```PowerShell
> winver
> ```