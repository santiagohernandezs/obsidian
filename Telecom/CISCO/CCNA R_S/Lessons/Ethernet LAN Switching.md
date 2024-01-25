![|500](https://i.imgur.com/nQVp5nl.png)
Here we have an ethernet frame, with a header an a trailer, lets look up the header.

## Header

![|525](https://i.imgur.com/HxFXHxC.png)

- Preamble: The **preamble** is a sequence of alternating 0s and 1s that marks the beginning of an Ethernet frame.
	- It is 7 bytes long (56 bits)
	- Allows devices to synchronize the receiver clocks.
- SFD (Start Frame Delimiter): Indicates the start of the actual frame.
	- It is 1 byte long (8 bits)
	- The last bit is a 1
- Destination: Has the destination direction.
	- 6 bytes long (48 bits)
- Source: Has the source direction.
- Type: Indicates the layer 3 protocol used in the encapsulated packet.
	- 2 bytes long (16 bits).
	- Represent the type of the length of the encapsulated packet.
	- A value of 1500 or less indicates the length of the encapsulated packet in bytes.
	- A value of 1536 or more indicates the type of protocol used in the encapsulated packet (usually IPv4 or IPv6) and the length is determined via other methods.

## Trailer

![|525](https://i.imgur.com/rRYv5l4.png)

- FCS (Frame Check Sequence): Used by the receiving devices to detect errors in the transmission.
	- 4 bytes long (32 bits).
	- Detect corrupting data by running CRC (Cyclic Redundancy Check) algorithm over the received data.

## Considerations
- The preamble and SFD usually are not considered part of the header because every ethernet frame have one of this, therefore the size of the Ethernet header  + trailer is 18 bytes.
- The minimum size for an ethernet frame (Header + Payload (Packet) + Trailer) is 64 bytes.
- 64 bytes - 18 bytes (Header + Trailer) = 46 bytes. So the packet has a minimum payload size is 46 bytes.
- If the minimum is not reached *padding bytes* are added, this bytes are all 0 (zeros).