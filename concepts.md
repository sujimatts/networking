Protocols
  Internet - wires connected via under the sea
  Why do we need protocols ?
    - diff purposes like emails, video transfer , file transfer has diff requirements and we have diff protocols for each purposes
  TCP - use when it have to transfer complete information (no data loss in b/w)
  UDP - when data-loss is fine (video conferenece, youtube streaming) (stateless conenction)
  HTTPS - secure web servers
  DHCP - automatically assigning IP addresses 
  
  Big files are transfered as chunks (not as whole)

  IP - decides which device, data to send to
  port - decides which application needs the data

Netowrks
  LAN - local network (ethernet, wifi)
  MAN - across city
  WAN - across countries (optical fibre cables)

Topologies - BUS, RING, STAR, TREE (BUS+STAR), MESH

OSI Model (open s/m inter-connected)
1. application
  - users interact with application (browsers,whtsapp etc)
2. presentation
  - converts the data into binary, encrypts, abstract (compressed)
3. session
  - managing (establishes)connections, authentication
4. transport
  - takes care how to transfer data, amount of data to transfer, error control(checksum)
5. network
  - transfer data to diff networks (to routers), forms IP packets
6. data-link
  - allows communication with hosts, physical addressing (MAC)
7. physical
  - defines the relationship between a device and a transmission medium, such as a copper or optical cable

TCP/IP Model (5 layers)
Application - Transport - Network - Data-link-Physical

Diff architectures
    client-server & peer2peer

Application - whatsapp
process - send msg, record video (features of apps)
thread - to record video [ open camera]. one process can have multiple threads
sockets - interface between program and internet.  two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.
ephemeral ports - When a client needs to communicate with a server, the client is assigned an ephemeral port on the other hand server listens on a registered port, which ranges from 1024 to 49151.
                - helps to receive data back to specific wjhtsapp mobile in a wifinetwork 

HTTP
  - app.layer protocol
  - uses TCP
  - stateless (no info is stored)
  - methods
    - GET, POST, PUT, DELETE
  - keepalive
  - status codes classes
    - 1xx - informational
    - 2xx- success
    - 3xx - redirect
    - 4xx - client error
    - 5xx - server side error
  - cookie - stored in (browsers
  - 3rd party cookies (For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited. Such a cookie is considered to be a 3rd party cookie.)

Throughput vs Bandwidth:
  - Consider bandwidth as a pipe and throughput as water. The larger the pipe or bandwidth is, the more water or data can flow through it at one time.
  - Bandwidth provides you with a theoretical measure of the maximum number of packets that can be transferred and throughput tells you the number of packets that are actually being successfully transferred
  
