# Task 5: Network Traffic Analysis with Wireshark

## Objective
Capture live network packets and identify basic protocols and traffic types using Wireshark.

## Tools Used
- Wireshark
- Linux command line


For capturing network traffic with Wireshark on Linux
sudo wireshark(Launch Wireshark with sudo privileges for packet capture)

1 Select your active network interface (usually eth0, wlan0, or ens33)
2 Click the blue shark fin icon to start capture
3 Generate traffic by browsing websites or using commands below
4 Click the red square to stop capture
5 Use filter bar to search for protocols (http, dns, tcp, etc.)

sudo tcpdump -i any -w capture.pcap -c 100(
sudo → run as root (tcpdump needs elevated privileges)
tcpdump → packet capture tool
-i any → capture on all network interfaces
-w capture.pcap → write captured packets to a file named capture.pcap
-c 100 → stop after 100 packets have been captured
)


wireshark capture.pcap(
wireshark → opens the Wireshark GUI (packet analyzer)
capture.pcap → the packet capture file to open
)

curl -I http://www.google.com(
curl → tool to make web requests
-I → send HEAD request (show headers only, no body)
http://www.google.com → target URL
)

nslookup google.com(
nslookup → DNS lookup tool
google.com → the domain you want to query
)

dig google.com(
dig → advanced DNS lookup tool
google.com → domain to query)

ping -c 4 google.com(
ping → checks network reachability
-c 4 → send 4 ICMP echo requests
google.com → destination to test
)

curl -I https://www.github.com(
curl → command-line web request tool
-I → send a HEAD request (show headers only, no body)
https://www.github.com → URL to request
)

sudo timeout 60 tcpdump -i any -w task5_capture.pcap (
sudo → run with root privileges
timeout 60 → stop the command after 60 seconds
tcpdump → packet capture tool
-i any → capture on all network interfaces
-w task5_capture.pcap → save packets to task5_capture.pcap
)

## Protocols Identified
- **TCP**: Transmission Control Protocol (reliable connection-oriented)
- **DNS**: Domain Name System (domain to IP resolution)
- **HTTP/HTTPS**: Hypertext Transfer Protocol (web traffic)
- **TLS**: Transport Layer Security (encrypted connections)

 
## Files
- `capture.pcap`: Packet capture file
- `report.md`: Detailed analysis of captured packets

## Key Learnings
- Hands-on experience with packet capture tools
- Understanding of network protocol communication
- Wireshark filtering techniques for protocol analysis
