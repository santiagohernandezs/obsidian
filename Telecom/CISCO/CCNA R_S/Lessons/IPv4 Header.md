![](https://i.imgur.com/fXMMSKk.png)

This is the IPv4 header.
## Fields
- Version: Indicates the version of IP in use, it can be IPv4 or IPv6. (4 bits long, 1/2 byte).
	- If IPv4 is in use it represents as 4 in binary (0100).
	- If IPv6 is in use it represents as 6 in binary (0110).
- Internet Header Length (IHL): The last field of the IPv4 header (Options) is variable in length, so this field is necessary to indicate the local length of the header.
	- Identifies the length of the header **in 4-byte increment**. If the value in this field is 5 that means that the actual value is 20 because $5 \cdot 4 = 20$
	- Minimum value is 5 (20 bytes) and the maximum is 15 (60 bytes).
	- Minimum IPv4 header length is 20 bytes.
	- Maximum IPv4 header length is 60 bytes.
- DSCP (Differentiated Services Code Point): Used for QoS (Quality of Service) (6bits 3/4 byte).
	- Used to prioritize delay-sensitive data (streaming, voice and video)
- ECN (Explicit Congestion Notification). (2 bits 1/4 byte).
	- Provides end-to-end notification of network congestion without dropping packages.
	- This is an optional field that requires both devices and the underlaying network to support it.
- Total Length: Indicates the total length of the packet (L3 Header + L4 Segment) (16 bits, 2 bytes):
	- Indicate the length in bytes.
	- Minimum value is 20 (IPv4 header with no encapsulated data).
	- Maximum value is 65535.
- Identification Field: If a packet is fragmented due to being too large. This field is used to identify witch packet the fragment belongs to. (16 bits, 2 bytes)
	- All fragments of the same packet will have their own IPv4 header with the same value in this field.
	- Packets are fragmented if larger than the MTU (Maximum Transmission Unit) witch usually is 1500 bytes.
- Flags: Used to control and identify fragments, the 3 bits work as the following explanation (3 bits)
	- Bit 0: Reserved, always set to 0
	- Bit 1: DF (Don't fragment), used to indicate a packet that should not be fragmented. If set to 1 will not be fragmented.
	- Bit 2: MF (More Fragment) set to 1 if are more fragment in packet, set to 0 for the last fragment.
- Fragment Offset: Used to indicate the position of the fragment within the original, unfragmented IP packet.
	- Allows fragmented packets to be reassembled even if the fragments arrive out of order.
