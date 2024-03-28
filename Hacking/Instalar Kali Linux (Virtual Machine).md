# Instalar Oracle VM VirtualBox con Kali Linux

Kali Linux es una distribución de Linux diseñada específicamente para realizar pruebas de seguridad y hacking ético. Oracle VM VirtualBox, por otro lado, es una plataforma de virtualización que permite ejecutar sistemas operativos dentro de máquinas virtuales en un entorno aislado. Combinar Kali Linux con Oracle VM VirtualBox proporciona una poderosa herramienta para practicar y desarrollar habilidades en el campo del hacking ético de manera segura y controlada.

## Descargar Oracle VM VirtualBox

Puedes descargar Oracle VM VirtualBox desde la [página oficial de VirtualBox](https://www.virtualbox.org/).

![Descargar VM](Descargarvmpagina.png)

Después de descargarlo, ejecuta el archivo `.exe` e instálalo por completo.

## Descargar Kali Linux

Puedes obtener la imagen de Kali Linux desde la [página oficial de Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines) en VirtualBox<sup>64</sup>. Haz clic en el símbolo de descarga y espera a que se complete la descarga.

![Instalar Kali Linux en VirtualBox](kalilinuxvminstall.png)

Una vez descargado, descomprime el archivo utilizando [Winrar](https://www.winrar.es/descargas) o [7-Zip](https://www.7-zip.org/).

![Archivos de Kali Linux](archivosdekalilinuxinstall.png)

## Instalar Kali Linux en VirtualBox

1. Abre VirtualBox y haz clic en `Añadir`.
![Instalar Linux en VirtualBox](oraclecomoinstalarlinux.png)

2. Selecciona el archivo "ISO" que hayas descargado previamente para usarlo en la máquina virtual.
![Configuración de Kali Linux en VirtualBox](ponerlinuxkalienvm.png)

3. Una vez configurado, la máquina virtual estará lista para su uso. Si es la primera vez que la utilizas, el usuario y contraseña por defecto son: `kali`.
![Kali Linux listo para usar](kalilinuxlistoparausar.png)

## Actualizar Kali Linux automáticamente (Obligatorio)

Puedes mantener tu sistema actualizado ejecutando la siguiente línea de comando en la terminal de Kali Linux. Esto asegurará un mejor desempeño y seguridad en tu sistema.

```Bash
sudo apt update && sudo apt upgrade -y


```

![Actualizar Kali Linux](update&upgrade-kalilinux.png)

## Instalar todas las herramientas de Kali Linux (Recomendado)

Si deseas habilitar más funciones en tu sistema Kali Linux, puedes instalar todas las herramientas disponibles con el siguiente comando:

```Bash
sudo apt install kali-linux-everything


```

![Instalar todas las herramientas de Kali Linux](kalilinux-everything.png)