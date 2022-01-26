# Notes - Day 13

1. What does it mean that web sockets are bidirectional? Communications mode that is capable of transmitting data in both directions (send and receive). <a href = "https://www.computerhope.com/jargon/b/bidirect.htm">"Source"</a> Why is this useful? It enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time. <a href = "https://www.amx.com/en/site_elements/benefits-and-applications-of-websockets#:~:text=BIDIRECTIONAL.,submit%20a%20request%20each%20time.">"Source"</a>

2. Does socket.io use HTTP? WebSocket uses HTTP as the initial transport mechanism, but keeps the TCP connection alive after the HTTP response is received so that it can be used for sending messages between client and server. <a href = "https://www.google.com/search?q=+Does+socket.io+use+HTTP%3F&rlz=1C1CHZN_enUS962US962&sxsrf=APq-WBt7x3MniEeRRoNcwhRV86IOLhdkrw%3A1643180697218&ei=mfLwYYvCDIe50PEPi_qcyAI&ved=0ahUKEwjL8oiO7c71AhWHHDQIHQs9BykQ4dUDCA8&uact=5&oq=+Does+socket.io+use+HTTP%3F&gs_lcp=Cgdnd3Mtd2l6EAMyBggAEBYQHjIFCAAQhgMyBQgAEIYDMgUIABCGAzIFCAAQhgMyBQgAEIYDOgUIIRCgAToFCAAQzQI6CAghEBYQHRAeOgUIIRCrAkoECEEYAEoECEYYAFAAWK0VYI4eaABwAngBgAH8AYgBoAWSAQU0LjEuMZgBAKABAqABAcABAQ&sclient=gws-wiz">"Source"</a> Why? So it can be used for sending messages between client and server.

3. What happens when a client emits an event? The client will emit when there is an event, and that is then received by a listener on the server side.

4. What happens when a server emits an event? The server then emits when there is an event that is received by a listener from the client side.

5. What happens if a client “misses” an event? The socket should continue listening for emitting events continuously. The events will buffer until reconnection. <a href = "https://socket.io/docs/v4/emitting-events/">"Source"</a>

6. How can we mitigate this? Using `volatile` events. <a href = "https://socket.io/docs/v4/emitting-events/">"Source"</a>

7. Document the following Vocabulary Terms:

- *Socket:* A socket is one endpoint of a two way communication link between two programs running on the network. <a href = "https://www.geeksforgeeks.org/socket-in-computer-network/">"Source"</a>
- *Web Socket:* WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. <a href = "https://en.wikipedia.org/wiki/WebSocket">"Source"</a> <a href = "https://www.geeksforgeeks.org/what-is-web-socket-and-how-it-is-different-from-the-http/">"Ref"</a>
- *Socket.io:* Socket.IO is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js. <a href = "https://en.wikipedia.org/wiki/Socket.IO">"Source"</a>
- *Client:* A piece of computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks.  <a href = "https://en.wikipedia.org/wiki/Client_(computing)#:~:text=In%20computing%2C%20a%20client%20is,by%20way%20of%20a%20network.">"Source"</a>
- *Server:* A piece of computer hardware or software that provides functionality for other programs or devices, called "clients". <a href = "https://en.wikipedia.org/wiki/Server_(computing)">"Source"</a>
- *OSI Model:* The Open Systems Interconnection (OSI) model describes seven layers that computer systems use to communicate over a network. Application; Presentation; Session; Transport; Network; Data Link; Physical. <a href = "https://www.imperva.com/learn/application-security/osi-model/">"Source"</a>
- *TCP Model:*  The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. Application; Transport; Internet; Network Access. <a href = "https://www.geeksforgeeks.org/tcp-ip-model/">"Source"</a>
- *TCP:* Transmission Control Protocol a communications standard that enables application programs and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks. <a href = "https://www.fortinet.com/resources/cyberglossary/tcp-ip">"Source"</a>
- *UDP:* User Datagram Protocol uses a simple connectionless communication model with a minimum of protocol mechanisms. UDP provides checksums for data integrity, and port numbers for addressing different functions at the source and destination of the datagram. <a href = "https://en.wikipedia.org/wiki/User_Datagram_Protocol">"Source"</a>
- *Packets:* In networking, a packet is a small segment of a larger message. Data sent over computer networks is divided into packets. These packets are then recombined by the computer or device that receives them. <a href = "https://www.cloudflare.com/learning/network-layer/what-is-a-packet/">"Source"</a>

<a href = "">"Source"</a>

**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**
