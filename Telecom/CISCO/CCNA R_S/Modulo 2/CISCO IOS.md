# 2.1, 2.2 Cisco IOS

Todos los dispositivos finales y dispositivos de red requieren un sistema operativo (OS). Como se muestra en la figura, la parte del Sistema Operativo que interactúa directamente con el hardware de la PC se conoce como kernel. La parte que interactúa con las aplicaciones y el usuario se conoce como shell. El usuario puede interactuar con el shell mediante la interfaz de línea de comandos (CLI) o la interfaz gráfica del usuario (GUI).

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Cisco-IOS-Sistema-Operativo.png)

Cuando se usa una CLI, el usuario interactúa directamente con el sistema en un entorno basado en texto ingresando comandos en el teclado en un símbolo del sistema, como se muestra en el ejemplo. El sistema ejecuta el comando y, por lo general, proporciona una respuesta en forma de texto. La CLI necesita muy poca sobrecarga para operar. Sin embargo, exige que el usuario tenga conocimientos de la estructura subyacente que controla el sistema.

# GUI

Permite al usuario interactuar con el sistema utilizando un entorno de icono gráficos, menús y ventanas. Sin embargo este no simepre puede proporcionar todas la funcionalidades que hay dsiponobles en la CLI. Las GUI también pueden fallar, colapsar o simplemente no operar como se les indica, por ello se suele acceder a los equipos de red mediante la CLI además de que esta consme menos recursos y es mucho más estable que la GUI.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/GUI-Windows.png)

La familia de sistemas operativos de red utilizados en muchos dispositivos Cisco se llama Cisco Internetwork Operating System (IOS). Cisco IOS se utiliza en muchos routers y switches de Cisco, independientemente del tipo o tamaño del dispositivo. Cada router o tipo de switch de dispositivo utiliza una versión diferente de Cisco IOS. Otros sistemas operativos de Cisco incluyen IOS XE, IOS XR y NX-OS.

**Nota**: El sistema operativo de los routers domésticos generalmente se denomina firmware. El método más frecuente para configurar un router doméstico consiste en utilizar un explorador web para acceder a una GUI.

# Proposito del OS

Los sistemas operativos de red son familiares al sistema operativo de una PC. Mediante un GUI, un sistema operativo permite que el usuario realice lo siguiente:

-   Utilice un mouse para hacer selecciones y ejecutar programas.
-   Introduzca texto y comando de texto.
-   Vea resultado en un monitor.

Un sistema operativo basado en CLI como el Cisco IOS en un switch o router permite que un técnico haga lo siguiente:

-   Utilice un teclado para ejecutar programas de red basados en CLI.
-   Utilice un teclado para introducir texto y comandos basados en texto.
-   Vea resultdos en un monitor.

Los dispositivos de red de Cisco ejecutan versiones especiales de Cisco IOS. La versión de IOS depende del tipo de dispositivo que se utilice y de las características necesarias.

# Métodos de acceso

| Metodos de acceso|Descripción|
|:---:|:---:|
|Cosola|Este es un puerto de administración físico que proporciona acceso fuera de banda a un dispositivo de Cisco. El acceso fuera de banda hace referencia al acceso por un canal de administración exclusivo que se usa únicamente con fines de mantenimiento del dispositivo. La ventaja de usar un puerto de consola es que el dispositivo es accesible incluso si no hay servicios de red configurados, como realizar la configuración inicial. Para una conexión de consola se requiere un equipo con software de emulación de terminal y un cable de consola especial para conectarse al dispositivo.|
|Secure Shell (SSH)|SSH es un método para establecer de manera remota una conexión CLI segura a través de una interfaz virtual por medio de una red. A diferencia de las conexiones de consola, las conexiones SSH requieren servicios de red activos en el dispositivo, incluida una interfaz activa configurada con una dirección. La mayoría de las versiones de Cisco IOS incluyen un servidor SSH y un cliente SSH que pueden utilizarse para establecer sesiones SSH con otros dispositivos.|
|Telnet|Telnet es un método inseguro para establecer una sesión CLI de manera remota a través de una interfaz virtual por medio de una red. A diferencia de SSH, Telnet no proporciona una conexión segura y encriptada y solo debe usarse en un entorno de laboratorio. La autenticación de usuario, las contraseñas y los comandos se envían por la red en texto simple. La mejor práctica es usar SSH en lugar de Telnet. Cisco IOS incluye un servidor Telnet y un cliente Telnet.|