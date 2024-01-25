# Caracterísitcas del cableado de cobre

Hoy en día el cable de cobre es el más común en las redes, de hecho cuneta con una varidad de ellos y cada cual se utilizan en situaciones específicas.

Las empresan utilizan cableado de cobre ya que es:

-   Muy económico.
-   Fáciles de instalar.
-   Tiene baja resistencia a la corriente eléctrica.

Sin embargo estos se ven limitados por la distancia y la interferencia de señal.

En el cableado de cobre, los datos se transmiten como pulsos eléctricos. Un detector en la **NIC** del dispositivo de destino debe recibir una señal que pueda decodificarse exitosamente para que coincidad con la señal enviada. Pero hayq ue tomar en cuenta que mientras más lejos viaja la señal más esta será deteriorada. Esto se denomina como **atenuación de señal**. Por este motivo hay estandares que desigan las distancias que se tienen que respetar al utilizar medios de este estilo.

Los valores de temporización y voltaje d elos pulsos eléctricos también son vulnerables a las interferencias de dos fuentes:

-   **Interferencia electromagnética (EMI) o interferencia de radiofrecuencia (RFI)**: Las señales EMI y RFI pueden distorcionar las señales de datos que transportan los medios de cobre. Las posibles fuentes de señales EMI y RFIincluyen las ondas de radio y dispositivos electromagnéticos, como las luces fluorescentes o los motores eléctricos.
-   **Crosstalk** : Se trata de la perturbación causada por los campos eléctreicos o magnéticos de una señal de un hilo a la señal de un hilo adyacente. En los circuitos telefónicos , el crosstalk puede provocar que se escuche parte de otra conversación de voz de un circuito adyacente.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Transmisi%C3%B3n-de-datos-afectada-por-interferencia.png)

1.  Se transmite la señal digitla pura.
2.  En el medio, hay una señal de interferencia.
3.  La señal digital está dañada.
4.  El quipo receptor lee una señal dañada.

# Electromagnetic Interferience (EMI) o Radio-Frequency Interferience (RFI)

Es la perturbación que ocurre en un circuito, componente o sistema electrónico causada por una fuente de radiación electromagnética externa o interna. Esta pertubación puede interrumpir, degradar o limitar le rendimiento de ese sistema.

## Clasificaión de las EMI

Se pueden clasficar en dos grupos:

1.  **Intencionadas**: Se refiere a interferencias por señales emitidas intencionalmente, con el propósito de producir un difusión en la víctima, es decir, un interferencia (Como ocurre en la denominada **Guerra Electrónica**)
2.  **No intencionadas**:

-   Se incluyen aquellas causadas por señales que tenían otro propósito y que accidentalmente dan un efecto no deseado en un tercero.
-   Aquellas emitidas no intencionalmente (equipos electrónicos, en su funcionamiento, normal, sistemas de conmutación, descargas electrostáticas, equipoos médicos, motores de inducción, etc.) que pueden resultar inocuas o pueden revelar informació sensible, como el contenido de una pantalla en la **''Interferencia de Van Eck''**, o simplementes si está encendido un dispositivo.

Para contrarrestar los efectos negativos de la EMI y la RFI, algunos tipos de cables de cobre se empaquetan con un blindaje metálico y requieren una conexión a tierra adecuada.

Para contrarrestar los efectos negativos del crosstalk, algunos tipos de cables de cobre tienen pares de hilos de circuitos opuestos trenzados que cancelan dicho tipo de interferencia en forma eficaz.

La susceptibilidad de los cables de cobre al ruido electrónico también se puede limitar utilizando estas recomendaciones:

-   La elección del tipo o la categoría de cable más adecuados a un entorno de red determinado.
-   El diseño de una infraestructura de cables para evitar las fuentes de interferencia posibles y conocidas en la estructura del edificio.
-   El uso de técnicas de cableado que incluyen el manejo y la terminación apropiados de los cables.

# Tipos de cableado de cobre


## Par trenzado no blindado o Unshielded twisted pair (UTP)

Es el medio más común. El cablado UTP, que se termina con conectores RJ-45, se utiliza para interconectar hosts de red con dispositivos intermediarios de red, como switchs y routers.

En las redes LAN, el cable UTP consta de cuatro pares de hilos codificados por colores que están trenzados entre sí y recubiertos por un revestimiento de plástico flexible que los protege contra daños físicos. El trenzado de hilo ayuda a proteger contra interferencias de señales de otros hilos.



1.  La cuboerta exterior protege los cables de cobre del daño físico.
2.  Los pares trenzados protegne la señal de interferencia.
3.  El aislamiento de plático codificado por colores aísla eléctricamnete los pares entre sí e dentifica cada par.

## Par tranzado blindado o Shielded twisted pair (STP)

El par trenazaod blindado **(STP)** proporciona una mejor protección contra ruido que el cableado UTP, sin embargo este es mucho más costoso, al igual que el cableado UTP, el STP utiliza el RJ-45

El cable STP combina las técnicas de blindaje para contrarrestar las interferencias EMI y RFI, y el tranzado de para contrarresatr el crosstalk. Par obtener emjor es resultados, los cable STP se terminan con conectores de datos STP blindados especiales, Si el cable no se conecta a tierra correctamente, el blindaje pued eactuar como antena y captar señales no deseadas.



1.  Cubeirta exterior.
2.  Ecudo trenzado o de aluminio.
3.  Escudos de aulminio.
4.  Pares trenzados.

## Cable coaxial

El cable coaxial obtiene su nombre dle hecho que hay dos conductores en el mismo eje.

-   Se utiliza un conductor de cobre par transmitir las señales electrónicas.
-   Una capa de ailamiento de plástico flexible que rodea al conductor de cobre.
-   Sobre este material aislante, hay una malla de cobre tejida o una hoja metálica que actúa como segundohilo en el circuito y como blindaje para le conductor interno. La segunda capa o blindaj reduce la cantidad de interferencia electromagnética externa.
-   La totalidad del cable está cubierta por un revestimiento para evitar daños físicos menores.

Esxisten diferentes tipos de conectores con cable coaxial. Los conectores Bayonet Neill-Concelman (BNC) o Bayoneta, tipo (N) y tipo (F) se muestrans en la figura.

Aunque el cable UTp ha reemplazado al cable coaxial, el diseño de cable coaxial de usan en las siguientes situaciones:

-   **Instalaciones inalámbricas**: Los cables coaxiales conectan las antenas a los dispositivos inalámbircos. También transportan energía de radiofrecuencia (RF) entre las antenas y el equipo de radio.
-   **Instalaciones de Internet por cable**: Los porveedores de servicios de cable proporcionanconectividad a Internet a sus clientes mediante el reemplazo de porciones cable coaxial y la admisión de elemntos de amplificación con cables de fibra óptica. sin embargo el cableado en las instlaciones del cliente sigue siendo coaxial.



1.  La cubierta exterior .
2.  Blindaje de cobre trenzado.
3.  Aislamiento plático.
4.  Conductor de cobre.