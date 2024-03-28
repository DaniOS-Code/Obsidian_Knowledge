1. Abre un editor de texto, como el Bloc de notas, y copia el siguiente código:

```Bash
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\kbdclass\Parameters]
"KeyboardDataQueueSize"=dword:00000020

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\mouclass\Parameters]
"MouseDataQueueSize"=dword:00000020

[HKEY_CURRENT_USER\Control Panel\Accessibility\Keyboard Response]
"DelayBeforeAcceptance"=dword:200

```

2. Pega el código en el editor de texto y luego guárdalo como un archivo con extensión `.reg`, por ejemplo, "MejorarResponsividad.reg". Asegúrate de que el tipo de archivo sea "Todos los archivos" al guardarlo.

3. Una vez que hayas guardado el archivo `.reg`, deberás ejecutarlo para aplicar los cambios en el registro de Windows. Haz doble clic en el archivo `.reg` que acabas de crear.

4. Windows mostrará una advertencia de que se realizarán cambios en el registro. Haz clic en "Sí" para confirmar que deseas realizar estos cambios.

5. Después de hacer clic en "Sí", los valores de registro se agregarán automáticamente y mejorarán la responsividad del teclado y el mouse.

6. Reinicia tu computadora para que los cambios surtan efecto.