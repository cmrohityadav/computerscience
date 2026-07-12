# Content

## Network
- 2 ya 2 se zyada devices jo aapas me communicate kar sakte hain
- Networking ka matlab hi communication hai.
- Agar ye(Laptop,Mobile,Printer etc) ek dusre se baat kar sakte hain ya data bhej sakte hain, to ye same network me hain

```txt
Example 1

Socho tumhare aur dost ke paas walkie-talkie hai
Rahul  <------->  Rahul
Ye ek chhota network hai.


Example 2 - Ghar ka WiFi

           WiFi Router
               |
----------------------------------
|          |          |          |
Laptop    Mobile      TV      Printer


Laptop connect hua.

↓
DHCP bola
↓
Le...
192.168.1.2

Dusra mobile aaya.
↓
DHCP bola
↓
Le...
192.168.1.3

TV aaya.
↓
DHCP bola
↓
Le...
192.168.1.4

```
```txt
192.168.y.x

192.168 = Private IP Range ka part hai.

y = Network ID (Router/Admin configure karta hai)

x = Host ID (DHCP ya Admin assign karta hai) / Host (Device)
```
- Example
```txt
Tumne router setup kiya
Tumne decide kiya:
Network = 192.168.5.x
Ab router ka IP ho sakta hai:
192.168.5.1
Ab DHCP devices ko dega:

Laptop   → 192.168.5.2

Mobile   → 192.168.5.3

TV       → 192.168.5.4

yeh Mobile,TV,etc sab ek Host hai
yeh pure Network ko LAN(Local Area Network)
```
### CIDR (Classless Inter-Domain Routing)
- CIDR Notation (/24, /16, /8) batata hai ki IP Address ki shuru ki kitni bits Network ke liye reserve hain aur kitni bits Host (Devices) ke liye hain
```bash
192.168.1.25
192      .168      .1       .25
8 bits   8 bits    8 bits   8 bits

Total = 32 bits



CIDR /24
192.168.1.25/24
192      .168      .1       .25
Network  Network   Network  Host

CIDR /16
192.168.1.25/16
192      .168      .1       .25
Network  Network   Host     Host


CIDR /8
10.5.20.30/8
10      .5      .20      .30
Network Host    Host     Host


CIDR /32
192.168.1.25/32
Network Network Network Network
Represents only one IP Address
Mostly used in:
                Firewall Rules
                Routing
                Access Control Lists (ACLs)

```
### Subnet
- Subnet Mask bas ye batata hai: IP ka kaunsa hissa Network hai aur kaunsa Host

```txt
IP Address
      AND
Subnet Mask
      ↓
Network Address
```























## IP Address
- IP Address ek Logical Address hai
- Jaise Hamare ghar ka address
- Computer ke paas do address hote hain
```txt
MAC Address = Physical Address
- MAC hardware ke andar hota hai

IP Address = Logical Address
- IP software se assign hota hai

```


```txt
192.168.1.10
Octet: har . seperate  to octet
11000000 10101000 00000001 00001010


8 bits each Octet
8 bits means 0-255 values

8*4=32 bits
Isliye IPv4 = 32-bit address


```

### Private IP vs Public IP

