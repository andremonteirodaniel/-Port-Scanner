
Simple Port Scanner (TCP)

A Python port scanning script using the native `socket` library. It checks the availability of TCP ports on a target host, helping to identify running services.

Features

TCP Scanning: Uses `socket.connect_ex` to attempt connections to specific ports, ideal for quick scanning.
Configured Timeout:** Sets a timeout of 0.5 seconds for each connection attempt to optimize speed.
Default Ports: If no port is specified, it scans a list of common ports (21, 22, 23, 25, 80, 443, 445, 8080, 8443, 3306, 139, 135).
Simple Output: Prints the port with the status "[+] <PORT> open" if the connection is successful (return code 0).

Prerequisites

This tool uses only the `socket` and `sys` libraries, which are native to Python. No additional installation is required.

Installation

1. Clone the repository:

bash

git clone https://github.com/andremonteirodaniel/-Port-Scanner.git

cd -Port-Scanner

Usage

Option 1: Using default ports

Provide only the target host. The default port list will be used.

``bash
python portscan.py <TARGET_HOST>

  Example: python portscan.py google.com

 Option 2: Specifying ports
Provide the target host and a comma-separated list of ports (no spaces).

'''bash

python portscan.py <TARGET_HOST> <COMMA_PORTS>

Example: python portscan.py google.com 22,80,443,8080

Important Technical Details

The scan uses `socket.connect_ex()`. A return code of `0` indicates that the port is open.

The timeout is set to `0.5` seconds per attempt.

If no port is provided, the default list includes: `21, 22, 23, 25, 80, 443, 445, 8080, 8443, 3306, 139, 135`.
