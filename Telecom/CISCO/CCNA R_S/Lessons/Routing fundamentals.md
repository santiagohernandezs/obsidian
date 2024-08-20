when `show ip route` command is triggered which is a command to display all routes configured in the router, the router itself will display some useful information.
![|725](https://i.imgur.com/CX7kvG0.png)

The **Codes** section displays all the different protocols supported by the router. The bottom section displays all the routes with there code and some info such as the ip and the interface to access that network

- Local (L): A route to the actual IP address configured on the interface. (with a /32 netmask)
- Connected (C): A route to the network the interface is connected to. (with the actual netmask configured on the interface)

When an interface is configured and enabled through `no shutdown` command, 2 routes will be added to the routing table; the connected and the local one.