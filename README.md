<p align=center>
<img src="https://github.com/ANG13T/netspionage/blob/master/assets/banner.png" />
  <br />
  <br />
  <span>
  <b> Network Analysis CLI framework that performs Network Scanning, OSINT, and Attack Detection</b>
  </span>
  <br>
</p>

<p align="center">
  <a href="#installation">Installation</a>
  &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#usage">Usage</a>
  &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#contributing">Contributing</a>
  &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#upcoming">Upcoming</a>
</p>

## Installation

```console
# clone the repo
git clone https://github.com/YAHYA950/netspionage.git

# change the working directory to netspionage
cd netspionage

# install the requirements
pip3 install -r requirements.txt
```

## Update Config [configuration.ini]
Adjust configuration settings such as WiFi Interface, Color, and Text File Logging
```
[Settings]
LogToTextFile=False
WiFiInterface=wlan0
Color=green
```

## Usage
In order to get started with netspionage just type:
```
python3 netspionage.py

OR

sudo -E python3 netspionage.py
```

## Further Configuration
```
# Ensure your Network Adapter is on Monitor Mode 
sudo airmon-ng start wlan0

ip a

# Find name of Network Adapter (ie. wlan0mon)

# Set Interface to Name

vim configuration.ini

WiFiInterface=wlan0mon
```

### Banner
```
                __             _                            
    ____  ___  / /__________  (_)___  ____  ____ _____ ____ 
   / __ \/ _ \/ __/ ___/ __ \/ / __ \/ __ \/ __ `/ __ `/ _ \
  / / / /  __/ /_(__  ) /_/ / / /_/ / / / / /_/ / /_/ /  __/
 /_/ /_/\___/\__/____/ .___/_/\____/_/ /_/\__,_/\__, /\___/ 
                    /_/                        /____/  
                    
 Created by Angelina Tsuboi [angelinatsuboi.net] V.0.0.1

 https://github.com/ANG13T/netspionage
 ----------------------------------------------------------------------------
 
 ENTER 1 - 4 TO SELECT OPTIONS

 1.  SCANNING                   Scan for IPs, nearby APs, ports, hosts, and more

 2.  RECONNAISSANCE             Gather  information  about nearby MAC addresses

 3.  DETECTION                  Detect for ARP Spoofing and SYN Flood attacks

 4.  EXIT                       Exit from netspionage to your terminal
 
```

**NETWORK SCANNER**

Gather information abuot devices connected to network such as IP address, MAC address, and OS.
```
netspionage >> 1
SCAN INPUT >> 1
NET IP ADDRESS (Eg: 192.168.1.1/24) >> 192.168.1.1/24
```

**WiFi SCANNER**

Gather information about nearby WiFi access points such as dBm Signal, SSID, channel, and encryption.
```
netspionage >> 1
SCAN INPUT >> 2
```

**PORT SCANNER**

Scan ports on a specified network to check if they are open or closed.
```
netspionage >> 1
SCAN INPUT >> 3
NET IP ADDRESS (Eg: 192.168.1.1/24) >> 192.168.1.1/24
```

**MAC ADDRESS RECON (CHOOSE)**

This option allows you to gather data about a selected device on the network via MAC address.
```
netspionage >> 2
RECON INPUT >> 1
NET IP ADDRESS (Eg: 192.168.1.1/24) >> 192.168.1.1/24
```

**MAC ADDRESS RECON (INPUT)**

This option allows you to gather data about a device via an inputted MAC address.
```
netspionage >> 2
RECON INPUT >> 2
MAC ADDRESS (Eg:08:00:69:02:01:FC) >> 08:00:69:02:01:FC
```

**DETECT ARP SPOOFING**

Detect for ARP Spoofing Attacks on your network.
```
netspionage >> 3
DETECT INPUT >> 1
NET IP ADDRESS (Eg: 192.168.1.1/24) >> 192.168.1.1/24
```

**DETECT TCP FLOODING**

Detect for TCP Flood Attacks on your network.
```
netspionage >> 3
DETECT INPUT >> 2
NET IP ADDRESS (Eg: 192.168.1.1/24) >> 192.168.1.1/24
TCP NUMBER (Eg: 80) >> 80
```

**HELP**

View all command options for netspionage.
```
netspionage >> help
```

**EXIT**

Exit netspionage from current terminal.
```
netspionage >> 4
Till next time!
```

## Contributing
We would love to have you help us with the development of netspionage. Read below on how to get started!
- Fork this Repository
- Contribute a change that either [resolve an issue](https://github.com/ANG13T/netspionage/issues) or [adds a new feature](#upcoming)
- Submit a PR for Review

## Upcoming
Here is a list of features we would like to integrate to netspionage in the upcoming versions:
- View/Edit config file (configuration.ini) through cli
- Detect for more OS in scanner (scanner.py -> get_os())

