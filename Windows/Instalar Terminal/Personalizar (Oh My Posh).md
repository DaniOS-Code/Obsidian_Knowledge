# Tutorial: Instalación y Configuración de Oh My Posh

Oh My Posh es una herramienta que te permite personalizar y mejorar la apariencia de la línea de comandos en Windows (Terminal de Windows). Puedes utilizar temas, iconos y estilos para hacer que tu terminal sea más atractiva y funcional. En este tutorial, aprenderás cómo instalar y configurar Oh My Posh en tu sistema.

## Paso 1: Requisitos Previos

Antes de comenzar, asegúrate de tener lo siguiente en tu sistema:

- **PowerShell**: Oh My Posh se ejecuta en PowerShell Core. Asegúrate de tener PowerShell Core instalado en tu sistema. Puedes descargarlo desde [la página oficial de PowerShell](https://github.com/PowerShell/PowerShell).

- **Git**: Si aún no tienes Git instalado, puedes descargarlo desde [Git for Windows](https://gitforwindows.org/).

- **Windows Terminal**: Se recomienda utilizar Windows Terminal para obtener la mejor experiencia con Oh My Posh. Puedes instalarlo desde la Microsoft Store o desde [GitHub](https://github.com/microsoft/terminal).

## Paso 2: Instalación de Oh My Posh

Para instalar Oh My Posh, sigue estos pasos:

1. Abre PowerShell Core como administrador. Puedes hacerlo buscando "PowerShell" en el menú Inicio, haciendo clic derecho en "Windows PowerShell" y seleccionando "Ejecutar como administrador".

2. Ejecuta el siguiente comando para instalar la versión más reciente de Oh My Posh desde PowerShell Gallery:

   ```PowerShell
   Install-Module -Name oh-my-posh -Scope CurrentUser
   ```

   Si te pide confirmación para instalar el módulo, selecciona "Sí" o "A" y presiona Enter.

3. A continuación, debes importar el módulo Oh My Posh en tu perfil de PowerShell para que se cargue automáticamente cuando inicies una sesión de PowerShell. Para hacerlo, ejecuta el siguiente comando:

   ```PowerShell
   Import-Module oh-my-posh
   ```

## Paso 3: Configuración de un Tema

Ahora que Oh My Posh está instalado, puedes configurar un tema. Los temas definen cómo se verá tu línea de comandos. Puedes encontrar una variedad de temas en [el repositorio de temas de Oh My Posh](https://github.com/ohmyposh/oh-my-posh-themes).

Para aplicar un tema, sigue estos pasos:

1. Elige un tema de [la lista de temas](https://github.com/ohmyposh/oh-my-posh-themes) o crea el tuyo propio siguiendo [las instrucciones](https://ohmyposh.dev/docs/themes).

2. Abre tu perfil de PowerShell para editarlo. Puedes abrirlo con el siguiente comando:

   ```Batch
   notepad $PROFILE
   ```

3. Agrega una línea al final de tu perfil de PowerShell para establecer el tema deseado. Por ejemplo:

   ```PowerShell
   Set-PoshPrompt -Theme Paradox
   ```

   Asegúrate de reemplazar "Paradox" con el nombre del tema que deseas utilizar.

4. Guarda y cierra el archivo de perfil.

5. Cierra y vuelve a abrir tu sesión de PowerShell o Windows Terminal para ver el tema aplicado.

## Paso 4: Personalización Adicional (Opcional)

Oh My Posh permite una personalización detallada, como cambiar los colores, los iconos y más. Puedes encontrar información sobre personalización en la [documentación oficial de Oh My Posh](https://ohmyposh.dev/docs/).