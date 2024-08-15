Keylogger con capturas de pantalla (Linux)

Este programa es un keylogger básico el cual registra las teclas presionadas en el sistema  en el que se ejecute y toma capturas de pantalla cada minuto a partir de que el programa se ejecute.Este programa es una herramienta que sirve para entender el funcionamiento de los eventos del teclado y la automatización de capturas de pantalla en lenguaje de programación C.

Características

Registro de teclas: Captura todas las teclas presionadas en un archivo de texto (keylogger.txt).
Captura de pantalla: Realiza capturas de pantalla cada minuto y las guarda en un directorio (screenshots).
Gestión de teclas especiales: Maneja teclas como Shift, AltGr y Caps Lock para capturar caracteres especiales.

Requisitos

Sistema operativo Linux.
Acceso a /dev/input/ para leer eventos del teclado (requiere permisos de root).
El programa scrot instalado para realizar capturas de pantalla.
Librerías de C (stdio.h, fcntl.h, unistd.h, linux/input.h, sys/stat.h, string.h, stdlib.h, errno.h, ctype.h, time.h, sys/types.h).

Instalación

Clonar el repositorio git clone https://github.com/dramirez1021/keylogger.git
Compilar el programa gcc -o keylogger_ss.c
Ejecutar el programa como root sudo./keylogger_ss

Instrucciones de uso

Ejecución: Al ejecutar el programa, este comenzará a registrar todas las teclas presionadas en el archivo keylogger.txt ubicado en la ruta /home/tu_usuario/Documentos/seguridad_informatica/. Además, creará un directorio llamado screenshots en la misma ruta, donde guardará capturas de pantalla cada minuto.

Finalización del programa: Para detener el programa, puedes usar Ctrl + C en la terminal donde se está ejecutando.

Acceso a los registros:
El archivo de registro de teclas (keylogger.txt) estará ubicado en /home/tu_usuario/Documentos/seguridad_informatica/.
Las capturas de pantalla estarán en el directorio /home/tu_usuario/Documentos/seguridad_informatica/screenshots/
sudo apt-get install scrot

nota: es importante cambiar las direcciones donde se guardaran los registros y las ss de lo contrario el codigo no compilara ya que no encontrara las direcciones.

Supuestos del Programa

Sistema Operativo: El programa está diseñado para sistemas Linux y se piensa que el dispositivo de entrada del teclado se encuentra en /dev/input/.

Permisos: El programa debe ser ejecutado con permisos de root para acceder a los eventos de teclado y crear directorios y tomar capturas de pantalla.

Dependencias: Se necesita que scrot esté instalado en el sistema. Si no es así, puedes instalarlo con: sudo apt-get install scrot

Casos de uso 

Monitoreo de entradas del teclado: Puedes usar este programa para monitorear y registrar las teclas presionadas en el sistema, puede servir para proyectos escolares o seguridad  informatica.
Captura de pantalla periódica: Además del registro de teclas, el programa captura la pantalla del que esté ejecutando el script. Esto podria usarse para el monitoreo de computo o espionaje.






