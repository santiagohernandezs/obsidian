# Limitaciones de IPv4

IPv4 todavía es´ta en uso hoy en día. Este tema trata sobre IPv6, que eventualmente reemplazará a IPv4. para comprender mejor por qué necesita conocer el protocolo IPv6, ayuda a conocer las limitaciones de IPv4 y las ventajas de IPv6.

A lo largo de los años, se han elaborado protocolos y procesos adicionales para hacer frente a los nuevos desafíos. Sin embargo, incluso con los cambios, IPv4 aún tiene tres grandes problemas:

-   **Agotamiento de la dirección IPv4**: IPv4 tiene un número limitado de direcciones públicas únicas disponibles. Si bien hay aproximadamente 4000millines de direcciones IPv4, el incremento en la cantidad de dsipositivos nuevos con IP habilitad, las conexiones constantes y el crecimiento potencial de regiones menos desarrolladas aumentaron la necesidad de direcciones.
-   **Falta de conectividad de extremo a extremo**: La traducción de direcciones de red (NAT) es una tecnología comúnmente implementada dentro de las redes IPv4. NAT proporciona una manera para que varios dispositivos compartan una única dirección IPv4 pública. Sin embargo, dado que la dirección IPv4 pública se comparte, se oculta la dircción IPv4 de un host de la red interna. Esto puede ser un problema para las tecnologías que necesitan conectividad completa.
-   **Mayor complejidad de la red**: mientras que NAT ha ampliado la vida útil de IPv4, solo se trataba de un mecanismo de transición de IPv6. NAT en sus diversas implementaciones cre una complejidad adicional en la red, creando latencia y haciendo más difícil la solución de problemas.

# Información general sobre IPv6

A principios de la década de 1990, los problemas con IPv4 preocuparon al **Grupo de trabajo de ingeniería de Internet (IETF)** que, en consecuencia, comenzó a buscar un reemplazo. Esto tuvo como resultado el desarrollo de IP versión 6 (IPv6). IPv6 supera las limitaciones de IPv4 y representa una mejora importante con características que se adaptan mejor a las demandas de red actuales y previsibles.

Las mejoras de IPv6 incluyen las siguientes:

-   **Menejo de paquetes mejorado**: Las direcciones IPv6 se basan en el direccionamiento jerárquico de 128 bits en lugar de IPv4 con 32 bits.
-   **Mejor manejo de paquetes**: El encabezado IPv6 se ha simplificado con menos campos.
-   **Elimina la necesidad de NAT**: Conuna cantidad tan grande de direcciones IPv6 públicas, no se necesita NAT entre una dirección IPv4 privada y una IPv4 pública

El espacio de las direcciones IPv4 de 32 bits ofrece aproximadamente 4.294.967.296 direcciones únicas. El espacio de direcciones IPv6 proporciona 340,282,366,920,938,463,463,374,607,431,768,211,456, o 340 undecillones de direcciones. Esto es aproximadamente equivalente a cada grano de arena en la Tierra.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Comparaci%C3%B3n-espacio-de-direcciones-IPv4-e-IPv6.png)

---

# Campos de encabezado de paquete IPv4 en el encabezado de paquete IPv6

Uno de las mejoras de diseño más importantes de IPv6 con respecto a IPv4 es el encabezado simplificado IPv6.

Por ejemplo, el encabezado IPv4 consiste en un encabezao de longitud variable de 20 octetos (hasta 60 bytes si se usa el campo de Opciones) y 12 campos de encabezado básicos, sin incluir el campos de Opciones y el campo de Relleno. IPv6 consta de 40 Octetos y o campos de enacbezado

Para IPv6, algunos campos se han mantenido igual, algunos campos han cambiado de nombre y posición, y algunos campos de IPv4 ya no son necesarios, como se destaca en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Encabezado-paquetes-IPv4-e-IPv6.png)

# Encabezado de paquetes IPv6

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Encabezado-de-Paquetes-IPv6.png)