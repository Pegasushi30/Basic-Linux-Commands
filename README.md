# How to Create Your Own Linux Command

You can create your own custom Linux command by following these simple steps:

1. Use the `nano` text editor to create a new shell script file named `networkdemo.sh` in your home directory:
    ```bash
    nano ~/networkdemo.sh
    ```

2. Make the shell script executable by changing its permissions:
    ```bash
    chmod +x ~/networkdemo.sh
    ```

3. Move the shell script to the `/usr/bin` directory to make it accessible system-wide:
    ```bash
    sudo mv ~/networkdemo.sh /usr/bin/networkdemo
    ```

## Example Shell Script

Below is an example shell script (`networkdemo.sh`) that provides a simple menu for performing network-related tasks:
```bash
Option a (-a): Executes a ping operation to check host reachability by sending ICMP echo request packets (ping -c 4 <address>).

Option b (-b): Performs a traceroute operation to trace the route taken by packets across an IP network to a specified destination (traceroute <address>).

Option c (-c): Conducts a DNS query to resolve a domain name to its corresponding IP address (nslookup <URL>).
```

```bash
#!/bin/bash

if [ $# -eq 0 ]; then
    echo "Usage: $0 -a|-b|-c"
    exit 1
fi


command=$1
shift

case $command in
    -a)
        ping -c 4 "$1"
        ;;
    -b)
        traceroute "$1"
        ;;
    -c)
        nslookup "$1"
        ;;
    *)
        echo "Invalid option! Options are: -a, -b, -c"
        exit 1
        ;;
esac
```


# Basic Networking Linux Commands
| Command                  | Description                                                 | Image |
|--------------------------|-------------------------------------------------------------|-------|
| ifconfig                 | Checks your network interfaces.                             |  ![Görsel Açıklaması](/images/471_1.jpg)    |
| traceroute google.com    | It's like your computer sending out little breadcrumbs to Google, hoping to find its way home. | ![Görsel Açıklaması](/images/471_2.jpg) |
| ping google.com          | Checks if Google is reachable.                              | ![Görsel Açıklaması](/images/471_3.jpg)    |
| nslookup                 | Finds IP addresses from domain names.                       | ![Görsel Açıklaması](/images/471_4.jpg)    |
| curl -I                  | Gets just the HTTP header of a URL.                         | ![Görsel Açıklaması](/images/471_5.jpg)    |
| ping -c 4 $address       | Sends four pings to an address.                             | ![Görsel Açıklaması](/images/471_6.jpg)    |
| httpie                   | A simple HTTP client.                                       | ![Görsel Açıklaması](/images/471.7.jpg)    |
| wget                     | Downloads files from the web.                               | ![Görsel Açıklaması](/images/471.8.jpg)    |
| tc                       | Controls traffic in Linux.                                  | ![Görsel Açıklaması](/images/471_9.jpg)    |
| dig            | Looks up DNS information.                                   | ![Görsel Açıklaması](/images/471_10_1.jpg)    |
| whois                    | Checks domain registration info.                            | ![Görsel Açıklaması](/images/471_11.jpg)    |
| ssh                      | Imagine your computer, sneaking into an exclusive VIP party with its own secret handshake. | ![Görsel Açıklaması](/images/471_12.jpg)    |
| scp                      | Securely copies files between hosts.                        | ![Görsel Açıklaması](/images/471_13.jpg)    |
| rsync                    | Efficiently syncs files and directories.                    | ![Görsel Açıklaması](/images/471_14.jpg)    |
| ngrep                    | Searches network traffic.                                   | ![Görsel Açıklaması](/images/471_15.jpg)    |
| tcpdump                  | Captures and analyzes network packets.                      | ![Görsel Açıklaması](/images/471_16.jpg)    |
| wireshark                | Analyzes network protocols.                                 | ![Görsel Açıklaması](/images/471_17_1.jpg) ![Görsel Açıklaması](/images/471_17_2.jpg)    |
| tshark                   | Command-line version of Wireshark.                          | ![Görsel Açıklaması](/images/471_18.jpg)    |
| tcpflow                  | Captures and stores TCP data.                               | ![Görsel Açıklaması](/images/471t_19.jpg)    |
| route                    | Manages IP routing tables.                                  | ![Görsel Açıklaması](/images/471_20.jpg)    |
| ip                       | Handles IP addresses and routes.                            | ![Görsel Açıklaması](/images/471_21.jpg)    |
| arp                      | Manages the ARP cache.                                      | ![Görsel Açıklaması](/images/471_22.jpg)    |
| mitmproxy                | Interactive HTTPS proxy.                                    | ![Görsel Açıklaması](/images/471_23.jpg)    |
| nmap                     | Scans for open ports and services.                          | ![Görsel Açıklaması](/images/471_24.jpg)    |
| zenmap                   | GUI for Nmap.                                               | ![Görsel Açıklaması](/images/471_25.jpg) ![Görsel Açıklaması](/images/471_25_2.jpg)     |
| openvpn                  | VPN solution.                                               | ![Görsel Açıklaması](/images/471_26.jpg)    |
| ftp/sftp                 | File transfer protocols.                                    | ![Görsel Açıklaması](/images/471_27.jpg)    |
| iptables                 | Controls IPv4 packet filtering.                             | ![Görsel Açıklaması](/images/471_28.jpg)    |
| mtr           | Traces packet routes.                                       | ![Görsel Açıklaması](/images/471_29.jpg)    |
| openssl                  | Handles secure communications.                              | ![Görsel Açıklaması](/images/471_30.jpg)    |



