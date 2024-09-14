- Paso 1: Crear el proceso OSPF

```
router ospf x
```

- Paso 2: Definir un RID dentro del proceso OSPF

```
router-id a.b.c.d
```

- Paso 3: Habilitar OSPF en las interfaces

```
ip ospf x area y
```

- Paso 4: Declarar interfaces pasivas (si es necesario)

```
ip ospf passive-interface | passive-interface default
```

- Paso 5: Declarar la ruta por defecto en el router de borde o GW

```
default-infomation originate always
```

Nota: luego de hacer esta configuración hay que declarar una ruta estática que lleva hacia intenet en el router de borde .

```
ip route a.b.c.d e.f.g.h i.j.k.l
```

## Opcionales
- Manipulación de contadores

Hello Interval
```
ip ospf hello-interval 10
```

Dead Interval
```
ip ospf dead-interval 40
```

- Manipulación de MTU

Al cambiar el MTU en un de las interfaces esto puede romper las adyacencias entre los vecinos para que OSPF no tome en cuenta este parámetro debemos indicarle que lo ignore.
```
ip mtu x
ip ospf mtu-ignore
```

- Manipulación del equal-cost multi-path (ECMP)
```
maximum-paths x
```