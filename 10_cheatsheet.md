# Linux Networking Commands Cheat Sheet

This document lists common Linux networking commands with short explanations for quick reference.

| Command | Description |
|---------|-------------|
| **ifconfig** | Displays or configures network interfaces (deprecated in favor of `ip` command). |
| **ifconfig eth0 up** | Brings the `eth0` interface up (activates it). |
| **ip addr** | Shows IP addresses assigned to all network interfaces. |
| **ip addr show** | Displays detailed IP address information for all interfaces. |
| **ip addr add 192.168.1.1/24 dev eth0** | Assigns the IP address `192.168.1.1` with subnet mask `/24` to `eth0`. |
| **ip link** | Displays link-layer (Ethernet) information for all interfaces. |
| **ip link show** | Shows status and properties of all network interfaces. |
| **ip link set eth0 down** | Disables the `eth0` interface. |
| **ip route** | Shows current routing table. |
| **ip route show** | Displays all routes in the routing table. |
| **ip route add default via <192.168.1.1>** | Adds a default gateway to route traffic via `192.168.1.1`. |
| **route** | Displays the kernel’s routing table (older command). |
| **route -n** | Shows routing table without resolving hostnames. |
| **route flush** | Clears all routing entries (requires root). |
| **route add default gw <192.168.1.1>** | Adds a default gateway using the `route` command. |
| **arp** | Displays and manipulates the ARP cache. |
| **arp -a** | Shows all ARP table entries. |
| **arp -n** | Displays ARP table without resolving names. |
| **arp -a -d** | Deletes all ARP entries. |
| **arp -d <ip>** | Deletes a specific ARP entry for the given IP. |
| **arp -s** | Adds a static ARP entry. |
| **iwconfig** | Displays or configures wireless network interfaces. |
| **iwconfig wlan0** | Shows wireless settings for `wlan0`. |
| **curl** | Transfers data from or to a URL (supports many protocols). |
| **wget** | Downloads files from the web. |
| **curl -o <link>** | Downloads a file from a URL and saves with the given filename. |
| **wget <link>** | Downloads file from a given URL. |
| **netstat** | Displays network connections, routing tables, and interface stats (deprecated in favor of `ss`). |
| **netstat -tuln** | Shows all listening TCP/UDP ports without DNS resolution. |
| **netstat -r** | Displays routing table. |
| **ss** | Modern replacement for `netstat` to display socket statistics. |
| **ss -tuln** | Lists listening TCP/UDP ports without DNS resolution. |
| **ss -i** | Shows detailed interface statistics. |
| **iftop** | Displays real-time bandwidth usage per connection. |
| **iftop -n** | Shows bandwidth usage without resolving hostnames. |
| **iftop -i eth0** | Monitors bandwidth on the `eth0` interface. |
| **tcpdump** | Captures and analyzes network packets. |
| **tcpdump -i <eth0>** | Captures packets on `eth0`. |
| **tcpdump -n <port 80>** | Captures packets on port 80 without resolving names. |
| **nc** / **netcat** / **ncat** | Reads/writes data across network connections (port scanning, file transfer, etc.). |
| **hping** | Packet generator and analyzer (used for testing firewalls, network performance). |
| **speedometer** | Measures and displays the speed of data transfer. |
| **vnstat** | Monitors network traffic statistics. |
| **socat** | Multipurpose data relay tool (TCP, UDP, serial, files). |
| **dig <example.com>** | Queries DNS servers for domain information. |
| **nslookup example.com** | Queries DNS records for a given domain. |
| **host example.com** | Looks up DNS information for a domain. |
| **hostname** | Displays the system’s hostname. |
| **hostname <myhost>** | Sets the system’s hostname to `<myhost>`. |
| **ping example.com** | Sends ICMP echo requests to test connectivity. |
| **traceroute example.com** | Traces the route packets take to a host. |
| **tracepath example.com** | Similar to traceroute but does not require root privileges. |
| **mtr example.com** | Combines ping and traceroute in real time. |
| **whois example.com** | Retrieves WHOIS information for a domain. |
| **ifplugstatus eth0** | Checks cable connection status for `eth0`. |
| **iperf** | Measures network bandwidth between two hosts. |
| **bwm-ng** | Displays real-time network bandwidth usage for interfaces. |
| **telnet** | Connects to a remote host on a given port (insecure). |
| **w** | Shows logged-in users and their activity. |
| **mail** | Sends and receives emails from the terminal. |
| **iw** | Modern tool to configure wireless devices. |
| **ngrep** | Network packet grep – searches for patterns in network traffic. |
| **ssh** | Securely connects to a remote host over SSH. |
| **scp** | Securely copies files between hosts using SSH. |
| **sftp** | Secure FTP client over SSH. |
| **iptables** | Configures firewall rules in Linux. |
| **snort** | Intrusion detection and prevention system. |
| **wireshark** | GUI network protocol analyzer. |
| **ufw** | Simplified firewall management tool for iptables. |

> **Note:** Some commands like `ifconfig`, `netstat`, and `route` are deprecated but still available in many systems. Use the modern `ip` and `ss` commands instead.
