En los XE podemos generar multiprocesos OSPF lo que nos permitirá tener un procesos IPv4 e IPv6 dentro de un solo proceso, a diferencia como pasa en el XR que estos deben mantenerse en procesos separados. A continuación la configuración a realizar.

```
router ospfv3 x
```

Donde *x* es el numero de proceso.

Ahora debemos declarar las familias para los protocolo v4 y v6

```
address-family { ipv4 | ipv6 } unicast
```

y luego declaramos el router-id y las interfaces pasivas

```
router-id a.b.c.d
passive-interface x
```

Una vez completado la configuración debemos aplicarla a las interefaces de la sigueinte manera.

```
ospfv3 x area y address-family { ipv4 | ipv6 }
```

Donde *x* es el numero de proceso y *y* es el area.
