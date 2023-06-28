# Movilidad
Al hablar de movimiento hacemos referencia al cambio de directorios dentro de Linux para hacer esto dentro de la terminal usaremos el siguiente comando.
```bash
cd x
```
Donde `cd` es el comando que nos permitirá navegar en la terminal y significa "Change Directory" y la x es el directortio (puede ser referido por su ruta absoluta o por su ruta relativa).
## Rutas de directorios
Una ruta es una lista de nombres de directorio separados por barras, seguida por un nombre de directorio o por el nombre de un archivo.
Existen tres tipos de rutas:
- Aboslutas
- Relativas
- Personales

![Imgur](https://i.imgur.com/7q4ikxL.png)
### Rutas Absolutas
Una ruta absoluta se basa en la raíz del árbol de Linux. Toda ruta absoluta empieza, pues, por `/`
Sea cual sea la ubicación actual donde se encuentre, se podrá referenciar el archivo notas del ejemplo anterior con la ruta `/home/willy/notas`.
### Rutas Relativas
Las rutas relativas dependen del directorio actual en donde se encuentra el usuario.
Sabiendo que cada directorio en el sistema contiene los archivos . (punto) y .. (punto-punto) que referencian respectivamente el propio directorio actual y el directorio padre, existen varias rutas relativas que designan el archivo notas en el ejemplo:

|Directorio Actual|Ruta Relativa Correspondiente|
|:--:|:--:|
|`/home`|`/willy/notas`|
|`/home/willy`|`./notas`|
|`/home/willy/colores`|`../notas`|

# Directorios
## Creación
Para crear un directorio disponemos del siguiente comando.
```bash
mkdir x
```
Donde `mkdir` es el comando que nos permitirá crear el directorio y significa "Make Directory" y x es el argumento que será el nombre del directorio.
## Borrado
Para borrar o eliminar un directorio utilizaremos el siguiente comando.
```bash
rmdir x
```
Donde `rmdir` es el comando que nos permitirá crear el directorio y significa "Remove Directory" y x es el argumento que será el nombre del directorio.
# Ficheros
## Creación
Para la creación de ficheros utilizaremos el sigueinte comando.
```bash
touch x
```
Donde `touch` es el comando que nos permitirá crear el fichero y x es el argumento que será el nombre del fichero.
## Borrado
Para borrar o eliminar un fichero utilizaremos el siguiente comando.
```bash
rm x
```
Donde `rm` es el comando que nos permitirá eliminar el fichero y significa "Remove" y x es el argumento que será el nombre del fichero.
# Otros Comandos
## echo
El comando Echo de Linux es uno de los comandos más utilizados en el sistema operativo Linux y te permite mostrar información en el Bash. **echo es** un  **comando** para la impresión de un texto en pantalla. **Es** utilizado en las terminales de los sistemas operativos como Unix, GNU/**Linux**, o MS-DOS; dentro de pequeños programas llamados scripts; y en ciertos lenguajes de programación tales como PHP.
Lo utilizaremos de la sisguiente manera
```bash
echo x
```
Donde `echo` es el comando que nos permitirá imprimir en pantalla y x lo que querramos imprimir, puede ser una string, un caracter, un archivo entre otros.
## cat
Se usa sobre todo para emitir el contenido de un archivo en la línea de comandos, aunque hay una gran cantidad de aplicaciones.
```bash
cat [Opciones] <Nombre(s) del archivo>
```

## mv
**mv** es un **comando** de Unix usado para mover o renombrar archivos o directorios del sistema de archivos. El archivo original es borrado y se crea un nuevo archivo con el mismo contenido, el nombre puede ser diferente o puede ser el mismo.
```bash
mv x
```
donde `mv` es el comando "Move" y x es el fichero o directorio que queremos mover.
## cp
El **comando cp** en GNU/**Linux** sirve para copiar un archivo o carpeta trabajando en la línea de **comandos**.
```bash
cp x y
```
Donde `cp` es el comando "Copy", x es el directorio o fichero que queremos copiar e y es la dirección a donde enviaremos la copia del archivo.
## grep
Es un comando que funciona como filtro para buscar ciertos parametros dentro de ficheros o directorios. El comando es el siguiente.
```bash
grep x y
```
Donde `grep` es el comando, x el parametro que queremos buscar e y el fichero o directorio donde vamos a buscar.
## sudo
Es una abreviación de "Super User Do" lo cual suplanta a "su" y nos permite ejecutar cualquiero comando ya que lo hacemos como si fuercemos un usuario **root**
## man
Es un comando de bastante importacia ya que contiene toda la información de los demás comandos en linux. Es una abreviación de "Manual" y da información acerca de cualquier comando.
```bash
man x
```
Donde `man` es el comando manual y x es el comando del que queremos obtener el manual.