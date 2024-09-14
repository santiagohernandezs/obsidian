## Ethernet
Ethernet is a collection of network protocols and standards, *is not a single thing*. 

## Bits and Bytes
A bit is the smallest value we can represent in information, it can be a 1 (one) or a 0 (zero). A byte is a collection of 8 bits, it used to represent more complex data and are sent through the network as a buffer.
$$
\Large 8 \hspace{.3cm} \text{bits} = 1 \hspace{.3cm} \text{byte}
$$
## Speed
Speed is measure in **bits per second** or **bps** not bytes per second o Bps. Therefore, we can use measures such as Kbps, Mbps, Gbps and so on and so forth.

![Data sent as bps (bits per second)|600](https://i.imgur.com/IVJB5HM.png)
> Data sent as bps (bits per second)

![|600](https://i.imgur.com/ck6s1o2.png)
> Data sent as Bps (byte per second) *the incorrect way in neteworking*

| Measure        | Value              |
| -------------- | ------------------ |
| 1 kilobit (Kb) | 1.000 bits         |
| 1 megabit (Mb) | 1.000.000 bits     |
| 1 gigabit (Gb) | 1.000.000.000 bits |
| 1 terabit (Tb)               | 1.000.000.000.000 bits                   |
## Ethernet Stadards
Are defined in the IEEE 802.3 standard in 1983 by the Institute of Electrical and Electronics Engineers (IEEE).

![|700](https://i.imgur.com/wtRmZax.png)

## UTP Cables
UTP stands for Unshielded Twisted Pair, unshielded means that the cable has not  any metallic shield and is vulnerable to electrical interference. Is the most typical cable for interconnecting devices, with 4 pairs of cables twisted in pairs, so it is 4 pairs of copper cables. But no all standards uses the 4 pairs.

| Standard               | Pairs usage       |
| ---------------------- | ----------------- |
| 10BASE-T and 100BASE-T | 2 Pairs (4 wires) |
| 1000BASE-T and 10GBASE-T                       | 4 Pairs (8 wires)                  |
### Types of cables and connections
There are different kinds of UTP cables based on the cable category

We also have two kinds of UTP connection **Straight-Through** connection and **Crossover** connection, it relies on the cable and the connection name are inherited by the kind of the cable, it could be a **Straight-Through Cable** or a **Crossover Cable**. The connection on the pins are really simple but it comes handy when we change one of the two devices. First, we have a connection between a pc or a client and a switch, in this scenario (using a 10BASE-T or 100BASE-T connection) we can use a straight-through cable (is called straight-through because connect the pins in a straight manner, the pin 1 with pin 1, pin 2 with pin 2, and so on). All the devices except a switch uses the pin 1 and 2 to transmit data and those pins are known as **Transmit** or **Tx**, the other pair are used to receive data, known as **Receive** or **Rx** and uses the pins 3 and 6.
![|675](https://i.imgur.com/18Wwftd.png)

What about of we change the left devices with a router? Well, nothing really change, as said before, the switch is the unique devices that uses different pins for transmit and receive data, so the connection still works.
![|675](https://i.imgur.com/HVw5FfK.png)

Now, what happens if we change the router with a switch? We have an issue, it uses the same pins to receive and transmit, so the straight cable would not work in this scenario.
![|675](https://i.imgur.com/42qh6UX.png)

As you could see, the pins from the straight cable, connect Rx with Rx and Tx wit Tx, yes it does not have any sense. In this cases, we use a **Crossover** cable.
![|675](https://i.imgur.com/YfR2VKz.png)

As the name says crossover, witch indicates the cables are crossed and with that configuration we connect Rx (left switch) with Tx (right switch) and Rx (right switch) with Tx (left switch). Cross over cables are use when the straight one does not work and the pins configuration match between devices. Now with this cable we can connect two computers or a computer to router, a router to a firewall etc.
![|675](https://i.imgur.com/wiJUeaQ.png)

Here's a list of devices and the pins configuration

| Device type | Transmit (Tx) pins | Receive (Rx) pins |
|:-----------:|:------------------:|:-----------------:|
|   Router    |      1 and 2       |      3 and 6      |
|  Firewall   |      1 and 2       |      3 and 6      |
|     PC      | 1 and 2                   | 3 and 6                  |
| Switch            |  3 and 6                   | 1 and 2                  |
## Fiber-Optic Cables
Are a 
![|675](https://i.imgur.com/U6OefdJ.png)
