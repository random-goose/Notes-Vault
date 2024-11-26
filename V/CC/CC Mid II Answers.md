# Switching
Switching in computer networks refers to the process of directing data packets between devices within a network or across different networks. It enables efficient data transmission by choosing the best path for data to travel from the source to the destination.

1. **Circuit Switching**
	A dedicated communication oath is established between the sender and receiver before data transfer begins 
	e.g.: Telephone networks
	
2. **Packet Switching**
	Data is divided into packets, each of which can take different paths to the destination. The packets are reassembled at the receiver
	e.g.: Internet Protocol
	
3. **Message Switching**
	Entire messages are stored at intermediate devices and forwarded to the next device only when the resources are available
	e.g.: Telegraph

## Circuit Switching
- A network switching method that establishes a dedicated communication path between source and destination
- Provides complete bandwidth and constant bit delay during the connection
- Commonly used in telecommunication

### Phases
1. Circuit Establishment
2. Data Transfer
3. Circuit Disconnection

### Multiplexing
- Frequency Division Multiplexing - FDM
- Time Division Multiplexing - TDM

### Advantages
- Guaranteed data rate
- No transmission delay after connection establishment
- High reliability
- Consistent quality of service
- Enhanced security
- Easy network management

### Disadvantages
- Limited scalability
- Resource inefficiency
- High cost
- Vulnerable to failure
- Not suitable for high or irregular traffic
- Lack of traffic prioritization


# Logical Addressing
refers to the assignment of unique identifiers called addresses to the devices in a network for communication. The two main protocols used on the Internet are IPv4 and IPv6

### IPv4
IP stands for Internet Protocol and the v4 stands for Version 4. It was brought to use within the ARPANET in 1983.
It is a unique address consisting of four octets of 8 bits each separated by decimal points
- is a 32-bit number
- represented in dotted-decimal format
- divided into 4 octets of 8 bits each
- each octet ranges from 0 to 255
- ex: 192.168.16.1

Classes
- It is divided into 4 classes A, B, C, D, E based on the range of the IP address
- Used for unicast, multicast, and experimental purposes

Address Space
- Supports approximately 4.3 Billion unique addresses - 2$^3$ $^2$ 
- Limited address space often requires Network Address Translation

Subnets
- Subnet Masks divide the address into network and host parts
- CIDR (Classless Inter-Domain Routing) allows flexible sub-netting (ex: 192.168.1.0/24)

Issues
- Exhaustion of IP addresses
- Lack of built-in security and mobility support

### IPv6
It is a 128-bit address which was made to replace the archaic IPv4, providing a larger address space and faster speeds. It is the current standard and deployed in mobile use cases too to identify devices among billions of others.
- is a 128-bit number
- represented in hexadecimal and is separated by colons
- contains 32 different digits separated into groups of 4
- ex: 2001:0db8:0000:000:0000:0000:0370:7334 or 2001:0db8::0370:7330

Address Space
- Supports 2^128
- Solves the address exhaustion problem

Address Types
- Unicast - one to one
- Multicast - one to many
- Anycast - to nearest node
- No Classes

Features
- Built in security
- Auto configuration
- Better QoS (Quality of Service)
- Co exists with IPv4

| IPv4                          | IPv6                        |
| ----------------------------- | --------------------------- |
| 32-bit                        | 128 Bit                     |
| Dotted Decimal                | Colon Seperated Hexadecimal |
| 4.3 Billion                   | 2^128                       |
| No Security                   | Built in IPSecurity         |
| 20 Byte Header                | 40 Byte Header              |
| Manual Configuration          | Auto Configuation           |
| Router and Host Fragmentation | Only Host Fragmentation     |

# UDP & TCP

| \                | UDP                     | TCP                         |
| ---------------- | ----------------------- | --------------------------- |
| Connection       | Connectionless          | Connection-Oriented         |
| Reliability      | Unreliable              | Very Reliable               |
| Speed            | High Speed              | Lower Speed                 |
| Flow Control     | None                    | Done thru Windowing         |
| Error Recovery   | No retransmission       | Automatic Retransmission    |
| Order of Packets | Unordered               | Guarentees correct ordering |
| Header Size      | 8 Bytes                 | 20 Bytes                    |
| Use Case         | Gaming, Streaming, VoIP | Web Browsing, email         |
| Overhead         | low                     | high                        |

UDP is used when speed is critical and packet loss can be tolerated; for example when streaming high definition video
TCP is used when the integrity of the data is most important and slower connection speeds can be tolerated like web surfing or emails


# Internet Protocols
### Email
POP3
- Post Office Protocol 3
- Used by email clients to retrieve emails from a mail server
- Once the mail is downloaded to the device, the mail is deleted from the server
IMAP
- Internet Message Access Protocol
- Unlike POP3 it keeps the mail on the server allowing access across multiple devices
SMTP
- Simple Mail Transfer Protocol
- Used for Sending Mails

### SMTP
Is a protocol to send mails over the internet.
Works with the mail clients like Gmail, Outlook, Thunderbird to send mails, ensuring the message is delivered properly to the correct recipient

- Works on the TCP over ports 25–587, 465 are used
- The client connects to the SMTP server, provides the recipient's email address, and transmits the mail
- The SMTP server forwards the email to the recipient's mail server

### HTTP
HyperText Transfer Protocol
it is the protocol use dot transmit web pages from a server to a browser, enabling both the request and response.
- A user enters a URL in the browser
- The browser sends an HTTP request to the web server for a specific resource
- The server responds with the requested data via an HTTP response
- Operates on port 80
- Stateless
- Used for Web Browsing

### HTTPS
HyperText Transfer Protocol Secure
It provides a secure channel to make HTTP connections by means of encrypting the data being transmitted between the client and the server
- Uses SSL/TLS (Secure Socket Layer / Transport Layer Security)
- The server provides a digital certificate to the client to verify the identity and integrity
- Even if the response is intercepted, the hacker cannot decrypt the data
- Runs on port 443

### DNS
Domain Name System
it is used to resolve the domain names such as x.com to its IP address so that the request can be sent to the right server
- When a user types in a domain name, a DNS query is sent to a DNS server
- The DNS server performs a lookup to get the IP address of the requested domain
- Once the IPA is found, traffic is routed to it
- runs on port 53

Domain Records
- A - maps domain name to IPv4 address
- AAAA - maps domain name to IPv6 address
- CNAME - maps domain name to another domain name
- MX - used for mail server

| Protocol | Port         |
| -------- | ------------ |
| SMTP     | 25, 587, 465 |
| HTTP     | 80           |
| HTTPS    | 443          |
| DNS      | 53           |

# Networking Protocols

### ARP
Address Resolution Protocol
- Used to map IP addresses to MAC (Media Access Control) addresses
- Works by sending an ARP Request
	- A device broadcasts a request similar to "Who has this IPA"
	- and the appropriate device response
- Ensures that devices on the same local network can communicate using hardware addresses
- Operates only on a subnet

### RARP
Reverse Address Resolution Protocol
- Reverse of ARP, used to find the IP address when the MAC address is known
- Used when a device does now have a static IP (like a NAS)
- Needs a dedicated RARP server
- Less common because of DHCP

### BOOTP
Bootstrap Protocol
- Used to assign IP addresses to a devie and provide a basic configuration details like the subnet mask, gatewat, and the address of a boot server
- The server responds with:
	- IP address for the client
	- Subnet mask, gateway address, and boot server
- Designed for diskless workstations to boot over the network
- Replaces by DHCP

### DHCP
Dynamic Host Configuration Protocol
Dynamically assigns IP Addresses and other network configuration parameters (subnet mask, gateway address etc.) to devices on a network
- Device broadcasts a DHCP Discover message when it joins a network
- DHCP Server responds with a DHCP Offer message when it's joining a network
- Client selects an offer and sends a DHCP Request
- The serves acknowledges with a DHCP acknowledgement

- Supports dynamic IP allocation
- IP Addresses are specifically leased for a period of time
- Used to manage large scale networks
- Uses port 67 (server) and 68 (client)

### CSMA/CD
Carrier Sense Multiple Access / Collision Detection
- Used in Half-Duplex wired Ethernet networks to manage data transmission and avoid collisions during communication
- Carrier Sense: checking for idle channel before transmitting
- Collusion Detection: checked by checking for spikes in voltage
	- Wait for a random time before retransmitting
- not needed n full-duplex or switched Ethernet networks

### CSMA/CA
Carrier Sense Multiple Access / Collision Avoidance
- Used in Wi-Fi (IEEE 802.11) networks as it is difficult to check for collisions in wireless networks
- Same Carrier Sense
- Collision Avoidance:
	- If Channel is empty an RTS request (Request To Send) is sent to the host
	- Host sends a CTS response (Clear To Send)
	- If the CTS is not received, it waits before sending again
- Limitation: High RTS/CTS overhead


[Intro]  
_[No, nothin' good starts in a getaway car](https://genius.com/13023284/Taylor-swift-getaway-car/No-nothin-good-starts-in-a-getaway-car)_  
  
[Verse 1]  
[It was the best of times, the worst of crimes](https://genius.com/13027344/Taylor-swift-getaway-car/It-was-the-best-of-times-the-worst-of-crimes)  
[I struck a match and blew your mind](https://genius.com/13078037/Taylor-swift-getaway-car/I-struck-a-match-and-blew-your-mind)  
But I didn’t mean it and you didn't see it  
[The ties were black, the lies were white  
In shades of gray in candlelight  
I wanted to leave him, I needed a reason](https://genius.com/13039679/Taylor-swift-getaway-car/The-ties-were-black-the-lies-were-white-in-shades-of-gray-in-candlelight-i-wanted-to-leave-him-i-needed-a-reason)  
  
[Pre-Chorus]  
["X" marks the spot where we fell apart  
He poisoned the well, I was lyin' to myself](https://genius.com/13040900/Taylor-swift-getaway-car/X-marks-the-spot-where-we-fell-apart-he-poisoned-the-well-i-was-lyin-to-myself)  
[I knew it from the first Old Fashioned, we were cursed](https://genius.com/13078260/Taylor-swift-getaway-car/I-knew-it-from-the-first-old-fashioned-we-were-cursed)  
[We never had a shotgun shot in the dark (Oh)](https://genius.com/13033110/Taylor-swift-getaway-car/We-never-had-a-shotgun-shot-in-the-dark-oh)  
  
[Chorus]  
[You were drivin’ the getaway car  
We were flyin', but we'd never get far](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Don't pretend it's such a mystery  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  
[Ridin' in a getaway car  
There were sirens in the beat of your heart](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Shoulda known I'd be the first to leave  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  

[

](https://viagogo.prf.hn/click/camref:1101l3DfTB/pubref:artist/destination:https%3A%2F%2Fwww.viagogo.com%2F_C-11113)

[

See Taylor Swift Live

Get tickets as low as $799

](https://viagogo.prf.hn/click/camref:1101l3DfTB/pubref:artist/destination:https%3A%2F%2Fwww.viagogo.com%2F_C-11113)

You might also like

[

But Daddy I Love Him

Taylor Swift



](https://genius.com/Taylor-swift-but-daddy-i-love-him-lyrics)[

loml

Taylor Swift



](https://genius.com/Taylor-swift-loml-lyrics)[

When Emma Falls in Love (Taylor’s Version) [From The Vault]

Taylor Swift



](https://genius.com/Taylor-swift-when-emma-falls-in-love-taylors-version-from-the-vault-lyrics)

[Post-Chorus]  
[In a getaway car (Oh-oh-oh)  
No, they never get far (Oh-oh-ah)](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[No, nothin' good starts in a getaway car](https://genius.com/13023284/Taylor-swift-getaway-car/No-nothin-good-starts-in-a-getaway-car)  
  
[Verse 2]  
[It was the great escape, the prison break](https://genius.com/26968090/Taylor-swift-getaway-car/It-was-the-great-escape-the-prison-break)  
The light of freedom on my face  
But you weren’t thinkin’ and I was just drinkin'  
[While he was runnin’ after us, I was screamin', "Go, go, go"  
But with three of us, honey, it's a sideshow  
And a circus ain't a love story and now we’re both sorry (We're both sorry)](https://genius.com/13039800/Taylor-swift-getaway-car/While-he-was-runnin-after-us-i-was-screamin-go-go-go-but-with-three-of-us-honey-its-a-sideshow-and-a-circus-aint-a-love-story-and-now-were-both-sorry-were-both-sorry)  
  
[Pre-Chorus]  
["X" marks the spot where we fell apart  
He poisoned the well, every man for himself](https://genius.com/13040900/Taylor-swift-getaway-car/X-marks-the-spot-where-we-fell-apart-he-poisoned-the-well-i-was-lyin-to-myself)  
[I knew it from the first Old Fashioned, we were cursed](https://genius.com/13078260/Taylor-swift-getaway-car/I-knew-it-from-the-first-old-fashioned-we-were-cursed)  
[It hit you like a shotgun shot to the heart (Oh)](https://genius.com/13033110/Taylor-swift-getaway-car/We-never-had-a-shotgun-shot-in-the-dark-oh)  
  
[Chorus]  
[You were drivin' the getaway car  
We were flyin', but we'd never get far](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Don't pretend it's such a mystery  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  
[Ridin' in a getaway car  
There were sirens in the beat of your heart](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Shoulda known I'd be the first to leave  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  

[Post-Chorus]  
[In a getaway car (Oh-oh-oh)  
No, they never get far (Oh-oh-ah)](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[No, nothin' good starts in a getaway car](https://genius.com/13023284/Taylor-swift-getaway-car/No-nothin-good-starts-in-a-getaway-car)  
  
[Bridge]  
[We were jet-set, Bonnie and Clyde (Oh-oh)](https://genius.com/13027302/Taylor-swift-getaway-car/We-were-jet-set-bonnie-and-clyde-oh-oh)  
[Until I switched to the other side, to the other side  
It's no surprise I turned you in (Oh-oh)](https://genius.com/13187051/Taylor-swift-getaway-car/Until-i-switched-to-the-other-side-to-the-other-side-its-no-surprise-i-turned-you-in-oh-oh)  
['Cause us traitors never win](https://genius.com/13109255/Taylor-swift-getaway-car/Cause-us-traitors-never-win)  
  
[Breakdown]  
[I'm in a getaway car](https://genius.com/13362283/Taylor-swift-getaway-car/Im-in-a-getaway-car)  
[I left you in a motel bar](https://genius.com/13218535/Taylor-swift-getaway-car/I-left-you-in-a-motel-bar)  
[Put the money in a bag and I stole the keys  
That was the last time you ever saw me (Oh)](https://genius.com/13209708/Taylor-swift-getaway-car/Put-the-money-in-a-bag-and-i-stole-the-keys-that-was-the-last-time-you-ever-saw-me-oh)  
  
[Chorus]  
[Drivin' the getaway car  
We were flyin', but we'd never get far (Don't pretend)](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Don't pretend it's such a mystery  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  
[Ridin' in a getaway car  
There were sirens in the beat of your heart (Shoulda known)](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[Shoulda known I'd be the first to leave  
Think about the place where you first met me](https://genius.com/13078449/Taylor-swift-getaway-car/Dont-pretend-its-such-a-mystery-think-about-the-place-where-you-first-met-me)  

[Post-Chorus]  
[In a getaway car (Oh-oh-oh)  
No, they never get far, oh-oh-ah](https://genius.com/13039714/Taylor-swift-getaway-car/You-were-drivin-the-getaway-car-we-were-flyin-but-wed-never-get-far)  
[No, nothin' good starts in a getaway car](https://genius.com/13023284/Taylor-swift-getaway-car/No-nothin-good-starts-in-a-getaway-car)  
  
[Outro]  
[I was ridin' in a getaway car  
I was cryin' in a getaway car  
I was dyin' in a getaway car  
Said goodbye in a getaway car  
Ridin' in a getaway car  
I was cryin' in a getaway car  
I was dyin' in a getaway car  
Said goodbye in a getaway car](https://genius.com/13039927/Taylor-swift-getaway-car/I-was-ridin-in-a-getaway-car-i-was-cryin-in-a-getaway-car-i-was-dyin-in-a-getaway-car-said-goodbye-in-a-getaway-car-ridin-in-a-getaway-car-i-was-cryin-in-a-getaway-car-i-was-dyin-in-a-getaway-car-said-goodbye-in-a-getaway-car)