# KSIP-Diff

KSIP-Diff is a powerful SIP packet inspector designed to identify misconfigurations in NAT rules, IP masquerading, DNAT, or SNAT on the network layer, as well as SIP packet modifications on the application layer. It allows users to send and receive SIP INVITE packets while detecting and highlighting any discrepancies in real-time, making it essential for VoIP troubleshooting and security analysis.

## Features
- Detects misconfigurations in NAT, DNAT, SNAT, and IP masquerading
- Identifies SIP packet modifications in real-time
- Send and receive SIP INVITE packets
- Detect and highlight packet modifications
- Works on Windows, Linux, and MacOS
- Supports interactive network interface selection
- Color-coded output for easy analysis
- Command-line interface with argument support

## Installation
KSIP-Diff requires Python 3.6 or higher. Clone the repository and install dependencies:

```sh
# Clone the repository
git clone https://github.com/yourusername/ksip-diff.git
cd ksip-diff
```

## Usage
KSIP-Diff can operate in two modes: **Sender** and **Receiver**.

### Run in Receiver Mode
```sh
python ksipdiff.py -R
```
This mode listens for incoming SIP INVITE packets and checks for modifications.

### Run in Sender Mode
```sh
python ksipdiff.py -S -si <Sender IP> -sp <Sender Port> -ri <Receiver IP> -rp <Receiver Port>
```
This mode sends a standard SIP INVITE packet to the specified receiver.

### Additional Options
- `-v` : Display version information
- `-si` : Specify sender IP address
- `-sp` : Specify sender port (default: 5060)
- `-ri` : Specify receiver IP address
- `-rp` : Specify receiver port (default: 5060)

## Example Usage
```sh
# Run receiver mode
karan@machine:~$ python ksipdiff.py -R

# Run sender mode
karan@machine:~$ python ksipdiff.py -S -si 192.168.1.10 -sp 5060 -ri 192.168.1.20 -rp 5060
```
---

## Download
[Ksipdiff.py](https://karan-modh.tech/download/ksipdiff.py)

---
