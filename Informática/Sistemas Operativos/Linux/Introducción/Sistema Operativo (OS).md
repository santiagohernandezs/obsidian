# Definición
Un sistema operativo es un intermediario entre el software y el hardware. Tiene como función controlar el hardware de un computaodr y asignar sus recursos al software. Además, también se encarga de asignar y decidir cuales procesos estará ejecutanto el hardware y en qué momento.

# Linux
Cuando hablamos de Linux en realidad estamos hablando de sistemas operativos basados en Linux, ya que, Linux no es un SO completo sino que es un nucleo Open Source que se puede utilizar para construir un SO completo.

A estos SO completo basados en Linux se les llama **distribuciones** de Linux entre las más concidas están:
- Ubuntu
- Mint
- Fedora
- Xubuntu

# Instalación de Ubuntu
La manera en la que Linux identifica sus discos duros es la siguiente.
```plaintext
/dev/sda
```
Es decir los discos duros se representan como `/dev/sd` y una letra como `a` o `b`. Por lo que, si tenemos varios discos, veriamos lo siguiente.
```plaintext
/dev/sda <- Primer disco
/dev/sdb <- Segundo disco
/dev/sdc <- Tercer disco
...
```
## Particiones
A la hora de instalar un sistema Linux es una buena práctica crear tres particiones.
- Primaria
- Swap
- General
### Primaria
Es la partición donde se encontrará el SO de manera aislada de las otras particiones por si en algun momento llega a fallar el SO no se pierda todos los datos del computador. En ese caso lo único que habría que hacer es reinstalar el SO en la partición corrupta.
Esta partición debe ser marcada como **primaria** y como sistema de ficheros debe utilizar el **ext4**
## Swap
Es una partición especial ya que, es usada cuando la memoria ram del computador se llena. Si se necesita de más recursos y la memoria ram está llena, toda la data inactiva en la ram se almacena en el Swap. Este tipo de partición no necesita de un punto de montaje.
## General
Es la partición que por lo general se lleva la mayor cantidad de almacenamiento ya que, es utilizada para que él o los usuarios depositen todos sus archivos como fotos, aplicaciones, videos en ella.
# Punto de Montaje
El punto de montaje es el directorio en el que se hace accesibles un nuevo sistema de archivos, un directorio o un archivo. Para montar un sistema de archivos o un directorio, el punto de montaje debe ser un directorio; y para montar un archivo, el punto de montaje debe ser un archivo.
Por lo general el punto de montaje de la partición primaria es `/` y el de la partición general es `/home`.