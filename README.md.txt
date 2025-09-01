Network Traffic Analysis with Wireshark

Project Objective
Capture, filter, and analyze network traffic using Wireshark.
Demonstrates understanding of protocols, packet structure, and network communication.

Tools Used
- Wireshark (latest version)
- Computer with active network connection (Wi-Fi/Ethernet)

Step-by-Step Process

Step 1: Start Capture
- Open Wireshark and select the active network interface.
- Leave the capture filter blank to record all traffic.
- Browse some websites to generate traffic.
- Screenshot: start_capture.png

Step 2: Protocol Hierarchy
- Analyze traffic breakdown: Statistics -> Protocol Hierarchy.
- Note common protocols (TCP, UDP, HTTP, DNS, HTTPS).
- Screenshot: protocol_hierarchy.png

Step 3: DNS Packet Analysis
- Apply display filter: dns
- Inspect DNS query packets.
- Expand Frame and DNS sections.
- Screenshot: dns_filter.png
- Screenshot: dns_filter2.png

Step 4: HTTP Packet Analysis
- Apply display filter: http (or tcp.port == 443 for HTTPS)
- Inspect HTTP GET/POST requests.

- Expand Frame and HTTP sections.
- Screenshot: http_request.png
- Screenshot: http_request2.png

Step 5: TCP Handshake
- Apply display filter: tcp.flags.syn == 1 && tcp.flags.ack == 0
- Inspect the initial SYN packet of a TCP handshake.
- Expand Frame and TCP sections.
- Screenshot: tcp_handshake.png
- Screenshot: tcp_handshake2.png
- Screenshot: tcp_handshake3.png

Key Findings
- Most traffic was over TCP and HTTPS.
- DNS queries revealed the domains visited during the capture.
- HTTP traffic is readable; HTTPS is encrypted.
- TCP handshake shows the 3-way connection setup process.

Reflection
This project taught me how to:
- Capture and analyze network traffic
- Filter specific protocols (DNS, HTTP, TCP)
- Interpret packet metadata (Frame, Protocol, Bytes)
- Identify encrypted vs unencrypted communication
- Build up my understanding of wireshark and gaining more knowledge about how to use the tool.