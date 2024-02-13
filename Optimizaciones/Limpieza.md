## Cómo Realizar una Limpieza del Disco en Windows

### Crear un Acceso Directo en el Escritorio

1. Haz clic derecho en el escritorio para abrir el menú contextual.
![Menú contextual](Menu-contextual-clean.png)

2. Selecciona "Nuevo" y luego "Acceso directo".

### Configurar el Acceso Directo

3. En la ventana emergente, ingresa la siguiente dirección en el campo "Ubicación del elemento" y haz clic en "Siguiente":
   ```Batch
   C:\Windows\System32\cleanmgr.exe
   ```
![Crear Acceso Directo](crear-acceso-directo-clean.png)

4. Asigna un nombre al acceso directo, por ejemplo, "Limpieza de Disco" y haz clic en "Finalizar".

### Ejecutar la Limpieza de Disco

5. Abre el acceso directo "Limpieza de Disco" que has creado en el escritorio.
![Acceso Directo](Pasted%20image%2020230703201841.png)

6. Selecciona la unidad que deseas limpiar (por ejemplo, "C:") y marca las opciones que desees limpiar, como "Archivos temporales de Internet" o "Archivos de programa descargados".
![Seleccionar Opciones de Limpieza](elegir-clean-disk.png)

### Ejecutar la Limpieza Automatizada (Opcional)

Si deseas ejecutar la limpieza de disco de forma automatizada utilizando un archivo `.bat`, sigue estos pasos:

1. Abre un editor de texto, como el Bloc de notas.
2. Copia y pega el siguiente código en el editor de texto:

```Batch
@echo off
:: BatchGotAdmin (Run as Admin code starts)
REM --> Check for permissions
>nul 2>&1 "%SYSTEMROOT%\system32\cacls.exe" "%SYSTEMROOT%\system32\config\system"

REM --> If error flag set, we do not have admin.
if '%errorlevel%' NEQ '0' (
    echo Requesting administrative privileges...
    goto UACPrompt
) else ( goto gotAdmin )

:UACPrompt
    echo Set UAC = CreateObject^("Shell.Application"^) > "%temp%\getadmin.vbs"
    set params = %*:"=""
    echo UAC.ShellExecute "cmd.exe", "/c %~s0 %params%", "", "runas", 1 >> "%temp%\getadmin.vbs"

    "%temp%\getadmin.vbs"
    del "%temp%\getadmin.vbs"
    exit /B

:gotAdmin
    pushd "%CD%"
    CD /D "%~dp0"
:: BatchGotAdmin

Color D
/s /f /q c:\windows\temp\*.*
rd /s /q c:\windows\temp
md c:\windows\temp
del /s /f /q C:\WINDOWS\Prefetch
del /s /f /q %temp%\*.*
rd /s /q %temp%
md %temp%
deltree /y c:\windows\tempor~1
deltree /y c:\windows\temp
deltree /y c:\windows\tmp
deltree /y c:\windows\ff*.tmp
deltree /y c:\windows\history
deltree /y c:\windows\cookies
deltree /y c:\windows\recent
deltree /y c:\windows\spool\printers
del c:\WIN386.SWP
cls 
FOR /F "tokens=1, 2 * " %%V IN ('bcdedit') DO SET adminTest=%%V
IF (%adminTest%)==(Access) goto noAdmin
for /F " tokens=*" %%G in ('wevtutil.exe el') DO (call :do_clear "%%G")
echo.
echo Event Logs have been cleared! ^<press any key^>
goto theEnd
:do_clear
echo clearing %1
wevtutil.exe cl %1
goto :eof
:noAdmin
echo You must run this script as an Administrator !
echo ^<press any key^>
cls
pause
```

3. Guarda el archivo con la extensión `.bat`, por ejemplo, "LimpiezaDeDisco.bat". Asegúrate de cambiar la extensión de `.txt` a `.bat`.

4. Ejecuta el archivo `.bat` como administrador haciendo doble click en él. Esto realizará una limpieza automática de varios elementos del sistema.