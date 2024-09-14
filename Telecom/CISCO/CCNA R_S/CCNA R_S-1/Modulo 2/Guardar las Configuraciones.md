# Archivos de configuración

Existen dos archivos de sistema que almacenan la configuración de dispositivos.

-   **startup-config** - Este es el archivo de configuración guardado que se almacenan en la NVRAM, contiene los comando que usará el dispositivo para iniciar o reiniciar.
-   **running-config** - Esto se almacena en la memoria de acceso aleatorio (RAM). Refleja la configuración actual. La modificación de una configuración en ejecución afecta el funcionamiento de un dispositivo Cisco de inmediato. La memoria RAM es volátil. Pierde todo el contenido cuando el dispositivo se apaga o se reinicia.

Si se corta la energía al dispositivo o si este se reinicia, se perderán todos los cambios de configuración a menos que se hayan guardado. Para guardar los cambios realizados en la configuración en ejecución en el archivo de configuración de inicio, utilice el comando **copy running-config startup-config** del modo EXEC privilegiado.

# Modificación de la configuración en ejecución

Si los cambios realizados en la configuracioón en ejecucuión no tienen el efecto deseado eliminando los ajuste no deseados individualmete o volviendo a cargar el dispositivo con el comando **reload**, como desventaja este comando eliminará la configuración en ejecución y estará fuera de línea hasta que termine de eliminar todo, lo que provocará tiempo de inactividad de la red.

Alternativamente, si los cambios no deseados se guardaron en la configuración de inicio, puede ser necesario borrar todas las configuraciones. Esto requiere borrar la configuración de inicio y reiniciar el dispositivo. La configuración de inicio se elimina mediante el **erase startup-config** comando del modo EXEC privilegiado. Una vez que se emite el comando, el switch le solicita confirmación. Press Enter to accept.

**Nota**: La memoria **FLASH** contiene el sistema operativo IOS y la **NVRAM** contiene la configuración de arranque.

# Captura de configuración a un carchivo de texto

Los archivos de configuración pueden guardarse y archivarse en un documento de texto. Esta secuencia de pasos asegura la disponibilidad de una copia utilizable del archivo de configuración para su modificación o reutilización en otra oportunidad.

Por ejemplo, suponga que se configuró un switch y que la configuración en ejecución se guardó en el dispositivo.

**Paso 1.** Abra el software de emulación de terminal, como PuTTY o Tera Term, que ya está conectado a un switch.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Software-de-emulaci%C3%B3n-de-terminal.png)

**Paso 2.** Habilite el inicio de sesión en el software del terminal y asigne un nombre y una ubicación de archivo para guardar el archivo de registro. La figura muestra que All session output se capturará en el archivo especificado (es decir, MySwitchLogs).

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Archivo-MySwitchLogs.png)

**Paso 3.** Ejecute el comando **show running-config** o **show startup-config** en el símbolo EXEC privilegiado. El texto que aparece en la ventana de la terminal se colocará en el archivo elegido.

```cisco
Switch# show running-config
Building configuration...
```

**Paso 4.** Desactive el inicio de sesión en el software del terminal. La figura muestra cómo deshabilitar el registro seleccionando None la opción de registro de sesión.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Configuraci%C3%B3n-PuTTY.png)

El archivo de texto creado se puede utilizar como un registro del modo en que se implementa actualmente el dispositivo. El archivo puede requerir edición antes de poder utilizarse para restaurar una configuración guardada a un dispositivo.

Para restaurar un archivo de configuración a un dispositivo:

**Paso 1.** Ingrese al modo de configuración global en el dispositivo.

**Paso 2.** Copie y pegue el archivo de texto en la ventana del terminal conectada al switch.

El texto en el archivo estará aplicado como comandos en la CLI y pasará a ser la configuración en ejecución en el dispositivo. Este es un método conveniente para configurar manualmente un dispositivo