# Nombre de los dispositivos

El primer comando de configuración en cualquier dispositivo debe ser darle un nombre de dispositivo único o nombre de host. De forma predeterminada, a todos los dispositivos se les asigna un nombre predeterminado de fábrica. Por ejemplo, un switch Cisco IOS es .

El problema es que si todos los awitches de una red se quedaran con sus nombres predeterminados, sería difícil identificar un dispositivo específico. Por ejemplo, ¿cómo sabrías que estás conectado al dispositivo correcto al acceder remotamente a través de una conexión SSH? El nombre de host proporciona la confirmación de que está conectado al dispositivo correcto.

El nombre predeterminado debe cambiarse a algo más descriptivo. Al elegir nombres atinadamente, resulta más fácil recordar, analizar e identificar los dispositivos de red. Estas son algunos pautas de nomenclatura importantes para los host:

-   Comenzar con una letra.
-   No contener espacios.
-   Finalizar con una letra o dígito.
-   Utilizar únicamente letras, dígitos, guiones.
-   Tener menos de 64 caracteres de longitud.

Una organización debe elegir una convención de nomenclatura que haga que sea fácil e intuitivo un dispositivo específico.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Cambiar-Nombres-de-host-en-Swtich.png)
	
Cuando se nombran los dispositivo de red, son fáciles de identificar para fines de configuración.

Para configurar el nombre del dispositivo usamos la siguiente suseción de comandos:

```cisco
Switch# configure terminal
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)# 
```

**NOTA**: Para devolver el switch al indicador predeterminado utilizar el comando **no hostname**

# Pautas de la contraseña

El uso de contraseñas débiles o fácilmente adivinadas sigue siendo la mayor preocuapción de seguridad de las organizaciones. Los dispositivos de red, incluso los router inlámbricos hogareños, siempre deben tener contraseñas configuradas para limitar el acceso administrativo.

Cisco IOS puede configurarse para utilizar contraseñas en modo jerárquico y permitir diferentes privilegios de acceso al dispositivo de red.

Todos los dispositivos de red deben limitar su acceso administrativo con contraseñas. Además todas las contraseñas deben estar encriptadas y deben proporcionarse notificaciones legales.

Al elegir las contraseñas, use algunas que sean seguras que no sean fáciles de adivinar. Hay algunos puntos clave a considerar al elegir las contraseñas:

-   Use contraseñas que tengan más de ocho caracteres de longitud.
-   Use una contraseña de letras mayúsculas y minúsculas, números, caracateres especiales o secuencias numéricas.
-   Evite el uso de la misma contraseña para todos los dispositivos.
-   No use palabras comunes fáciles de adivinar

# Configuración de contraseñas

## Proteger acceso por consola

```cisco
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line console 0
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
SW-Floor-1(config-line)# end
Sw-Floor-1#
```

# Proteger modo privilegiado

```cisco
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# enable secret cisco
Sw-Floor-1(config)# end
Sw-Floor-1#
```

## Proteger VTY (Virtual Teletype)

```cisco
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password cisco 
Sw-Floor-1(config-line)# login 
SW-Floor-1(config-line)# end
Sw-Floor-1#
```

# Encriptación de las contraseñas

Los archivos startup-config y running-config muestran la mayoría de las contraseñas en plain text. esto es una amenaza ya que cualquiera puede verlas si consigue acceder a estos archivos, para ello se utiliza el comando **service password-encryption**.

```cisco
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# service password-encryption
Sw-Floor-1(config)#
```

El comando aplica un cifrado débil a todas las contraseñas no encriptadas. Esta encriptación solo se aplica a las contraseñas del archivo de configuración; no a las contraseñas mientras se envían a través de los medios. El propósito de este comando es evitar que individuos no autorizados vean las contraseñas en el archivo de configuración.

Al aplicar la encriptación vería algo como esto si ejecuta el comando **show running-config**.

```cisco
SW-Floor-1(config)# end
Sw-Floor-1# show running-config
!
!
line con 0
password 7 094F471A1A0A 
login
!
line vty 0 4
password 7 03095A0F034F38435B49150A1819
login
!
!
end
```

# Mensaje de Aviso

Aunque solicitar contraseñas es una forma de mantener al personal no autorizado fuera de la red, es vital proporcionar un método para declarar que solo el personal autorizado debe intentar acceder al dispositivo. Para hacerlo, agregue un aviso a la salida del dispositivo. Los avisos pueden ser una parte importante en los procesos legales en el caso de una demanda por el ingreso no autorizado a un dispositivo. Algunos sistemas legales no permiten la acusación, y ni siquiera el monitoreo de los usuarios, a menos que haya una notificación visible.
```cisco
Sw-Floor-1# configure terminal 
Sw-Floor-1(config)# banner motd #Authorized Access Only#
```