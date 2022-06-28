Reference guide for scanning networks with Nmap.

Table of Contents

1.  [What is Nmap?](https://aacle.github.io/nmap#what-is-nmap)

2.  [How to Use Nmap](https://aacle.github.io/nmap#how-to-use-nmap)

    1.  [Command Line](https://aacle.github.io/nmap#command-line)

3.  [Basic Scanning Techniques](https://aacle.github.io/nmap#basic-scanning-techniques)

    1.  [Scan a Single Target](https://aacle.github.io/nmap#scan-a-single-target)

    2.  [Scan Multiple Targets](https://aacle.github.io/nmap#scan-multiple-targets)

    3.  [Scan a List of Targets](https://aacle.github.io/nmap#scan-a-list-of-targets)

    4.  [Scan a Range of Hosts](https://aacle.github.io/nmap#scan-a-range-of-hosts)

    5.  [Scan an Entire Subnet](https://aacle.github.io/nmap#scan-an-entire-subnet)

    6.  [Scan Random Hosts](https://aacle.github.io/nmap#scan-random-hosts)

    7.  [Exclude Targets From a Scan](https://aacle.github.io/nmap#exclude-targets-from-a-scan)

    8.  [Exclude Targets Using a List](https://aacle.github.io/nmap#exclude-targets-using-a-list)

    9.  [Perform an Aggresive Scan](https://aacle.github.io/nmap#perform-an-aggressive-scan)

    10.  [Scan an IPv6 Target](https://aacle.github.io/nmap#scan-an-ipv6-target)

4.  [Port Scanning Options](https://aacle.github.io/nmap#port-scanning-options)

    1.  [Perform a Fast Scan](https://aacle.github.io/nmap#perform-a-fast-scan)

    2.  [Scan Specific Ports](https://aacle.github.io/nmap#scan-specific-ports)

    3.  [Scan Ports by Name](https://aacle.github.io/nmap#scan-ports-by-name)

    4.  [Scan Ports by Protocol](https://aacle.github.io/nmap#scan-ports-by-protocol)

    5.  [Scan All Ports](https://aacle.github.io/nmap#scan-all-ports)

    6.  [Scan Top Ports](https://aacle.github.io/nmap#scan-top-ports)

    7.  [Perform a Sequential Port Scan](https://aacle.github.io/nmap#perform-a-sequential-port-scan)

    8.  [Attempt to Guess an Unknown OS](https://aacle.github.io/nmap#attempt-to-guess-an-unkown-os)

    9.  [Service Version Detection](https://aacle.github.io/nmap#service-version-detection)

    10.  [Troubleshoot Version Scan](https://aacle.github.io/nmap#troubleshoot-version-scan)

    11.  [Perform a RPC Scan](https://aacle.github.io/nmap#perform-a-rpc-scan)

5.  [Discovery Options](https://aacle.github.io/nmap#discovery-options)

    1.  [Perform a Ping Only Scan](https://aacle.github.io/nmap#perform-a-ping-only-scan)

    2.  [Do Not Ping](https://aacle.github.io/nmap#do-not-ping)

    3.  [TCP SYN Ping](https://aacle.github.io/nmap#tcp-syn-ping)

    4.  [TCP ACK Ping](https://aacle.github.io/nmap#tcp-ack-ping)

    5.  [UDP Ping](https://aacle.github.io/nmap#udp-ping)

    6.  [SCTP INIT Ping](https://aacle.github.io/nmap#sctp-init-ping)

    7.  [ICMP Echo Ping](https://aacle.github.io/nmap#icmp-echo-ping)

    8.  [ICMP Timestamp Ping](https://aacle.github.io/nmap#icmp-timestamp-ping)

    9.  [ICMP Address Mask Ping](https://aacle.github.io/nmap#icmp-address-mask-ping)

    10.  [IP Protocol Ping](https://aacle.github.io/nmap#ip-protocol-ping)

    11.  [ARP Ping](https://aacle.github.io/nmap#arp-ping)

    12.  [Traceroute](https://aacle.github.io/nmap#traceroute)

    13.  [Force Reverse DNS Resolution](https://aacle.github.io/nmap#force-reverse-dns-resolution)

    14.  [Disable Reverse DNS Resolution](https://aacle.github.io/nmap#disable-reverse-dns-resolution)

    15.  [Alternative DNS Lookup](https://aacle.github.io/nmap#alternate-dns-lookup)

    16.  [Manually Specify DNS Server](https://aacle.github.io/nmap#manually-specify-dns-server)

    17.  [Create a Host List](https://aacle.github.io/nmap#create-a-host-list)

6.  [Firewall Evasion Techniques](https://aacle.github.io/nmap#firewall-evasion-techniques)

    1.  [Fragment Packets](https://aacle.github.io/nmap#fragment-packets)

    2.  [Specify a Specific MTU](https://aacle.github.io/nmap#specify-a-specify-mtu)

    3.  [Use a Decoy](https://aacle.github.io/nmap#use-a-decoy)

    4.  [Idle Zombie Scan](https://aacle.github.io/nmap#idle-zombie-scan)

    5.  [Manually Specify a Source Port](https://aacle.github.io/nmap#manually-specify-a-source-port)

    6.  [Append Random Data](https://aacle.github.io/nmap#append-random-data)

    7.  [Randomize Target Scan Order](https://aacle.github.io/nmap#randomize-target-scan-order)

    8.  [Spoof MAC Address](https://aacle.github.io/nmap#spoof-mac-address)

    9.  [Send Bad Checksums](https://aacle.github.io/nmap#send-bad-checksums)

7.  [Advanced Scanning Functions](https://aacle.github.io/nmap#advanced-scanning-functions)

    1.  [TCP SYN Scan](https://aacle.github.io/nmap#tcp-syn-scan)

    2.  [TCP Connect Scan](https://aacle.github.io/nmap#tcp-connect-scan)

    3.  [UDP Scan](https://aacle.github.io/nmap#udp-scan)

    4.  [TCP NULL Scan](https://aacle.github.io/nmap#tcp-null-scan)

    5.  [TCP FIN Scan](https://aacle.github.io/nmap#tcp-fin-scan)

    6.  [Xmas Scan](https://aacle.github.io/nmap#xmas-scan)

    7.  [TCP ACK Scan](https://aacle.github.io/nmap#tcp-ack-scan)

    8.  [Custom TCP Scan](https://aacle.github.io/nmap#custom-tcp-scan)

    9.  [IP Protocol Scan](https://aacle.github.io/nmap#ip-protocol-scan)

    10.  [Send Raw Ethernet Packets](https://aacle.github.io/nmap#send-raw-ethernet-packets)

    11.  [Send IP Packets](https://aacle.github.io/nmap#send-ip-packets)

8.  [Timing Options](https://aacle.github.io/nmap#timing-options)

    1.  [Timing Templates](https://aacle.github.io/nmap#timing-templates)

    2.  [Set the Packet TTL](https://aacle.github.io/nmap#set-the-packet-ttl)

    3.  [Minimum Number of Parallel Operations](https://aacle.github.io/nmap#minimum-number-of-parallel-operations)

    4.  [Maximum Number of Parallel Operations](https://aacle.github.io/nmap#maximum-number-of-parallel-operations)

    5.  [Minimum Host Group Size](https://aacle.github.io/nmap#minimum-host-group-size)

    6.  [Maximum Host Group Size](https://aacle.github.io/nmap#maximum-host-group-size)

    7.  [Maximum RTT Timeout](https://aacle.github.io/nmap#maximum-rtt-timeout)

    8.  [Initial RTT TImeout](https://aacle.github.io/nmap#initial-rtt-timeout)

    9.  [Maximum Number of Retries](https://aacle.github.io/nmap#maximum-number-of-retries)

    10.  [Host Timeout](https://aacle.github.io/nmap#host-timeout)

    11.  [Minimum Scan Delay](https://aacle.github.io/nmap#minimum-scan-delay)

    12.  [Maximum Scan Delay](https://aacle.github.io/nmap#maximum-scan-delay)

    13.  [Minimum Packet Rate](https://aacle.github.io/nmap#minimum-packet-rate)

    14.  [Maximum Packet Rate](https://aacle.github.io/nmap#maximum-packet-rate)

    15.  [Defeat Reset Rate Limits](https://aacle.github.io/nmap#defeat-reset-rate-limits)

9.  [Output Options](https://aacle.github.io/nmap#output-options)

    1.  [Save Output to a Text File](https://aacle.github.io/nmap#save-output-to-a-text-file)

    2.  [Save Output to a XML File](https://aacle.github.io/nmap#save-output-to-a-xml-file)

    3.  [Grepable Output](https://aacle.github.io/nmap#grepable-output)

    4.  [Output All Supported File Types](https://aacle.github.io/nmap#output-all-supported-file-types)

    5.  [Periodically Display Statistics](https://aacle.github.io/nmap#periodically-display-statistics)

    6.  [1337 Output](https://aacle.github.io/nmap#1337-output)

10.  [Compare Scans](https://aacle.github.io/nmap#compare-scans)

    1.  [Comparison Using Ndiff](https://aacle.github.io/nmap#comparison-using-ndiff)

    2.  [Ndiff Verbose Mode](https://aacle.github.io/nmap#ndiff-verbose-mode)

    3.  [XML Output Mode](https://aacle.github.io/nmap#xml-output-mode)

11. [Troubleshooting and Debugging](https://aacle.github.io/nmap#troubleshooting-and-debugging)

    1.  [Get Help](https://aacle.github.io/nmap#get-help)

    2.  [Display Nmap Version](https://aacle.github.io/nmap#display-nmap-version)

    3.  [Verbose Output](https://aacle.github.io/nmap#verbose-output)

    4.  [Debugging](https://aacle.github.io/nmap#debugging)

    5.  [Display Port State Reason](https://aacle.github.io/nmap#display-port-state-reason)

    6.  [Only Display Open Ports](https://aacle.github.io/nmap#only-display-open-ports)

    7.  [Trace Packets](https://aacle.github.io/nmap#trace-packets)

    8.  [Display Host Networking](https://aacle.github.io/nmap#display-host-networking)

    9.  [Specify a Network Interface](https://aacle.github.io/nmap#specify-a-network-interface)

12. Nmap Scripting Engine

    1.  [Execute Individual Scripts](https://aacle.github.io/nmap#execute-individual-scripts)

    2.  [Execute Multiple Scripts](https://aacle.github.io/nmap#execute-multiple-scripts)

    3.  [Execute Scripts by Category](https://aacle.github.io/nmap#execute-scripts-by-category)

    4.  [Execute Multiple Script Categories](https://aacle.github.io/nmap#execute-multiple-script-categories)

    5.  [Troubleshoot Scripts](https://aacle.github.io/nmap#troubleshoot-scripts)

    6.  [Update the Script Database](https://aacle.github.io/nmap#update-the-script-database)

## [](https://aacle.github.io/nmap#what-is-nmap)What is Nmap?

Nmap ("Network Mapper") is a free and open source utility for network discovery and security auditing. Many systems and network administrators also find it useful for tasks such as network inventory, managing service upgrade schedules, and monitoring host or service uptime. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running. It was designed to rapidly scan large networks, but works fine against single hosts.

## [](https://aacle.github.io/nmap#how-to-use-nmap)How to Use Nmap

Nmap can be used in a variety of ways depending on the user's level of technical expertise.

| Technical Expertise | Usage |

| :-- | :-- |

| Beginner | [Zenmap](https://nmap.org/zenmap/) the graphical user interface for Nmap |

| Intermediate | [Command line](https://nmap.org/) |

| Advanced | Python scripting with the [Python-Nmap](https://pypi.org/project/python-nmap/) package |

### [](https://aacle.github.io/nmap#command-line)Command Line

```shell

nmap [ <Scan Type> ...] [ <Options> ] { <target specification> }

```

## [](https://aacle.github.io/nmap#basic-scanning-techniques)Basic Scanning Techniques

The `-s` switch determines the type of scan to perform.

| Nmap Switch | Description |

| :-- | :-- |

| \-sA | ACK scan |

| \-sF | FIN scan |

| \-sI | IDLE scan |

| \-sL | DNS scan (a.k.a. list scan) |

| \-sN | NULL scan |

| \-sO | Protocol scan |

| \-sP | Ping scan |

| \-sR | RPC scan |

| \-sS | SYN scan |

| \-sT | TCP connect scan |

| \-sW | Windows scan |

| \-sX | XMAS scan |

### [](https://aacle.github.io/nmap#scan-a-single-target)Scan a Single Target

```shell

nmap [target]

```

### [](https://aacle.github.io/nmap#scan-multiple-targets)Scan Multiple Targets

```shell

nmap [target1, target2, etc]

```

### [](https://aacle.github.io/nmap#scan-a-list-of-targets)Scan a List of Targets

```shell

nmap -iL [list.txt]

```

### [](https://aacle.github.io/nmap#scan-a-range-of-hosts)Scan a Range of Hosts

```shell

nmap [range of IP addresses]

```

### [](https://aacle.github.io/nmap#scan-an-entire-subnet)Scan an Entire Subnet

```shell

nmap [ip address/cdir]

```

### [](https://aacle.github.io/nmap#scan-random-hosts)Scan Random Hosts

```shell

nmap -iR [number]

```

### [](https://aacle.github.io/nmap#exclude-targets-from-a-scan)Exclude Targets From a Scan

```shell

nmap [targets] --exclude [targets]

```

### [](https://aacle.github.io/nmap#exclude-targets-using-a-list)Exclude Targets Using a List

```shell

nmap [targets] --excludefile [list.txt]

```

### [](https://aacle.github.io/nmap#perform-an-aggresive-scan)Perform an Aggresive Scan

```shell

nmap -A [target]

```

### [](https://aacle.github.io/nmap#scan-an-ipv6-target)Scan an IPv6 Target

```shell

nmap -6 [target]

```

## [](https://aacle.github.io/nmap#port-scanning-options)Port Scanning Options

### [](https://aacle.github.io/nmap#perform-a-fast-scan)Perform a Fast Scan

```shell

nmap -F [target]

```

### [](https://aacle.github.io/nmap#scan-specific-ports)Scan Specific Ports

```shell

nmap -p [port(s)] [target]

```

### [](https://aacle.github.io/nmap#scan-ports-by-name)Scan Ports by Name

```shell

nmap -p [port name(s)] [target]

```

### [](https://aacle.github.io/nmap#scan-ports-by-protocol)Scan Ports by Protocol

```shell

nmap -sU -sT -p U:[ports],T:[ports] [target]

```

### [](https://aacle.github.io/nmap#scan-all-ports)Scan All Ports

```shell

nmap -p 1-65535 [target]

```

### [](https://aacle.github.io/nmap#scan-top-ports)Scan Top Ports

```shell

nmap --top-ports [number] [target]

```

### [](https://aacle.github.io/nmap#perform-a-sequential-port-scan)Perform a Sequential Port Scan

```shell

nmap -r [target]

```

### [](https://aacle.github.io/nmap#attempt-to-guess-an-unknown-os)Attempt to Guess an Unknown OS

```shell

nmap -O --osscan-guess [target]

```

### [](https://aacle.github.io/nmap#service-version-detection)Service Version Detection

```shell

nmap -sV [target]

```

### [](https://aacle.github.io/nmap#troubleshoot-version-scan)Troubleshoot Version Scan

```shell

nmap -sV --version-trace [target]

```

### [](https://aacle.github.io/nmap#perform-a-rpc-scan)Perform a RPC Scan

```shell

nmap -sR [target]

```

## [](https://aacle.github.io/nmap#discovery-options)Discovery Options

Host Discovery The `-p` switch determines the type of ping to perform.

| Nmap Switch | Description |

| :-- | :-- |

| \-PI | ICMP ping |

| \-Po | No ping |

| \-PS | SYN ping |

| \-PT | TCP ping |

### [](https://aacle.github.io/nmap#perform-a-ping-only-scan)Perform a Ping Only Scan

```shell

nmap -sn [target]

```

### [](https://aacle.github.io/nmap#do-not-ping)Do Not Ping

```shell

nmap -Pn [target]

```

### [](https://aacle.github.io/nmap#tcp-syn-ping)TCP SYN Ping

```shell

nmap -PS [target]

```

### [](https://aacle.github.io/nmap#tcp-ack-ping)TCP ACK Ping

```shell

nmap -PA [target]

```

### [](https://aacle.github.io/nmap#udp-ping)UDP Ping

```shell

nmap -PU [target]

```

### [](https://aacle.github.io/nmap#sctp-init-ping)SCTP INIT Ping

```shell

nmap -PY [target]

```

### [](https://aacle.github.io/nmap#icmp-echo-ping)ICMP Echo Ping

```shell

nmap -PE [target]

```

### [](https://aacle.github.io/nmap#icmp-timestamp-ping)ICMP Timestamp Ping

```shell

nmap -PP [target]

```

### [](https://aacle.github.io/nmap#icmp-address-mask-ping)ICMP Address Mask Ping

```shell

nmap -PM [target]

```

### [](https://aacle.github.io/nmap#ip-protocol-ping)IP Protocol Ping

```shell

nmap -PO [target]

```

### [](https://aacle.github.io/nmap#arp-ping)ARP ping

```shell

nmap -PR [target]

```

### [](https://aacle.github.io/nmap#traceroute)Traceroute

```shell

nmap --traceroute [target]

```

### [](https://aacle.github.io/nmap#force-reverse-dns-resolution)Force Reverse DNS Resolution

```shell

nmap -R [target]

```

### [](https://aacle.github.io/nmap#disable-reverse-dns-resolution)Disable Reverse DNS Resolution

```shell

nmap -n [target]

```

### [](https://aacle.github.io/nmap#alternative-dns-lookup)Alternative DNS Lookup

```shell

nmap --system-dns [target]

```

### [](https://aacle.github.io/nmap#manually-specify-dns-server)Manually Specify DNS Server

Can specify a single server or multiple.

```shell

nmap --dns-servers [servers] [target]

```

### [](https://aacle.github.io/nmap#create-a-host-list)Create a Host List

```shell

nmap -sL [targets]

```

## [](https://aacle.github.io/nmap#port-specification-and-scan-order)Port Specification and Scan Order

| Nmap Switch | Description |

| :-- | :-- |

## [](https://aacle.github.io/nmap#serviceversion-detection)Service/Version Detection

| Nmap Switch | Description |

| :-- | :-- |

| \-sV | Enumerates software versions |

## [](https://aacle.github.io/nmap#script-scan)Script Scan

| Nmap Switch | Description |

| :-- | :-- |

| \-sC | Run all default scripts |

## [](https://aacle.github.io/nmap#os-detection)OS Detection

| Nmap Switch | Description |

| :-- | :-- |

## [](https://aacle.github.io/nmap#timing-and-performance)Timing and Performance

The `-t` switch determines the speed and stealth performed.

| Nmap Switch | Description |

| :-- | :-- |

| \-T0 | Serial, slowest scan |

| \-T1 | Serial, slow scan |

| \-T2 | Serial, normal speed scan |

| \-T3 | Parallel, normal speed scan |

| \-T4 | Parallel, fast scan |

Not specifying a `T` value will default to `-T3`, or normal speed.

## [](https://aacle.github.io/nmap#firewall-evasion-techniques)Firewall Evasion Techniques

### [](https://aacle.github.io/nmap#firewallids-evasion-and-spoofing)Firewall/IDS Evasion and Spoofing

| Nmap Switch | Description |

| :-- | :-- |

### [](https://aacle.github.io/nmap#fragment-packets)Fragment Packets

```shell

nmap -f [target]

```

### [](https://aacle.github.io/nmap#specify-a-specific-mtu)Specify a Specific MTU

```shell

nmap --mtu [MTU] [target]

```

### [](https://aacle.github.io/nmap#use-a-decoy)Use a Decoy

```shell

nmap -D RND:[number] [target]

```

### [](https://aacle.github.io/nmap#idle-zombie-scan)Idle Zombie Scan

```shell

nmap -sI [zombie] [target]

```

### [](https://aacle.github.io/nmap#manually-specify-a-source-port)Manually Specify a Source Port

```shell

nmap --source-port [port] [target]

```

### [](https://aacle.github.io/nmap#append-random-data)Append Random Data

```shell

nmap --data-length [size] [target]

```

### [](https://aacle.github.io/nmap#randomize-target-scan-order)Randomize Target Scan Order

```shell

nmap --randomize-hosts [target]

```

### [](https://aacle.github.io/nmap#spoof-mac-address)Spoof MAC Address

```shell

nmap --spoof-mac [MAC|0|vendor] [target]

```

### [](https://aacle.github.io/nmap#send-bad-checksums)Send Bad Checksums

```shell

nmap --badsum [target]

```

## [](https://aacle.github.io/nmap#advanced-scanning-functions)Advanced Scanning Functions

### [](https://aacle.github.io/nmap#tcp-syn-scan)TCP SYN Scan

```shell

nmap -sS [target]

```

### [](https://aacle.github.io/nmap#tcp-connect-scan)TCP Connect Scan

    nmap -sT [target]

    

### [](https://aacle.github.io/nmap#udp-scan)UDP Scan

```shell

nmap -sU [target]

```

### [](https://aacle.github.io/nmap#tcp-null-scan)TCP NULL Scan

```shell

nmap -sN [target]

```

### [](https://aacle.github.io/nmap#tcp-fin-scan)TCP FIN Scan

```shell

nmap -sF [target]

```

### [](https://aacle.github.io/nmap#xmas-scan)Xmas Scan

```shell

nmap -sA [target]

```

### [](https://aacle.github.io/nmap#tcp-ack-scan)TCP ACK Scan

```shell

nmap -sA [target]

```

### [](https://aacle.github.io/nmap#custom-tcp-scan)Custom TCP Scan

```shell

nmap --scanflags [flags] [target]

```

### [](https://aacle.github.io/nmap#ip-protocol-scan)IP Protocol Scan

```shell

nmap -sO [target]

```

### [](https://aacle.github.io/nmap#send-raw-ethernet-packets)Send Raw Ethernet Packets

```shell

nmap --send-eth [target]

```

### [](https://aacle.github.io/nmap#send-ip-packets)Send IP Packets

```shell

nmap --send-ip [target]

```

## [](https://aacle.github.io/nmap#timing-options)Timing Options

### [](https://aacle.github.io/nmap#timing-templates)Timing Templates

```shell

nmap -T[0-5] [target]

```

### [](https://aacle.github.io/nmap#set-the-packet-ttl)Set the Packet TTL

```shell

nmap --ttl [time] [target]

```

### [](https://aacle.github.io/nmap#minimum-number-of-parallel-operations)Minimum NUmber of Parallel Operations

```shell

nmap --min-parallelism [number] [target]

```

### [](https://aacle.github.io/nmap#maximum-number-of-parallel-operations)Maximum Number of Parallel Operations

```shell

nmap --max-parallelism [number] [target]

```

### [](https://aacle.github.io/nmap#minimum-host-group-size)Minimum Host Group Size

```shell

nmap --min-hostgroup [number] [targets]

```

### [](https://aacle.github.io/nmap#maximum-host-group-size)Maximum Host Group Size

```shell

nmap --max-hostgroup [number] [targets]

```

### [](https://aacle.github.io/nmap#maximum-rtt-timeout)Maximum RTT Timeout

```shell

nmap --initial-rtt-timeout [time] [target]

```

### [](https://aacle.github.io/nmap#initial-rtt-timeout)Initial RTT Timeout

```shell

nmap --max-rtt-timeout [TTL] [target]

```

### [](https://aacle.github.io/nmap#maximum-number-of-retries)Maximum Number of Retries

```shell

nmap --max-retries [number] [target]

```

### [](https://aacle.github.io/nmap#host-timeout)Host Timeout

```shell

nmap --host-timeout [time] [target]

```

### [](https://aacle.github.io/nmap#minimum-scan-delay)Minimum Scan Delay

```shell

nmap --scan-delay [time] [target]

```

### [](https://aacle.github.io/nmap#maxmimum-scan-delay)Maxmimum Scan Delay

```shell

nmap --max-scan-delay [time] [target]

```

### [](https://aacle.github.io/nmap#minimum-packet-rate)Minimum Packet Rate

```shell

nmap --min-rate [number] [target]

```

### [](https://aacle.github.io/nmap#maximum-packet-rate)Maximum Packet Rate

```shell

nmap --max-rate [number] [target]

```

### [](https://aacle.github.io/nmap#defeat-reset-rate-limits)Defeat Reset Rate Limits

```shell

nmap --defeat-rst-ratelimit [target]

```

## [](https://aacle.github.io/nmap#output-options)Output Options

| Nmap Switch | Description |

| :-- | :-- |

| `-oN` | Normal output |

| `-oX` | XML output |

| `-oA` | Normal, XML, and Grepable format all at once |

### [](https://aacle.github.io/nmap#save-output-to-a-text-file)Save Output to a Text File

```shell

nmap -oN [scan.txt] [target]

```

### [](https://aacle.github.io/nmap#save-output-to-a-xml-file)Save Output to a XML File

```shell

nmap -oX [scan.xml] [target]

```

### [](https://aacle.github.io/nmap#grepable-output)Grepable Output

```shell

nmap -oG [scan.txt] [target]

```

### [](https://aacle.github.io/nmap#output-all-supported-file-types)Output All Supported File Types

```shell

nmap -oA [path/filename] [target]

```

### [](https://aacle.github.io/nmap#periodically-display-statistics)Periodically Display Statistics

```shell

nmap --stats-every [time] [target]

```

### [](https://aacle.github.io/nmap#1337-output)1337 Output

```shell

nmap -oS [scan.txt] [target]

```

## [](https://aacle.github.io/nmap#compare-scans)Compare Scans

### [](https://aacle.github.io/nmap#comparison-using-ndiff)Comparison Using Ndiff

```shell

ndiff [scan1.xml] [scan2.xml]

```

### [](https://aacle.github.io/nmap#ndiff-verbose-mode)Ndiff Verbose Mode

```shell

ndiff -v [scan1.xml] [scan2.xml]

```

### [](https://aacle.github.io/nmap#xml-output-mode)XML Output Mode

```shell

ndiff --xml [scan1.xml] [scan2.xml]

```

## [](https://aacle.github.io/nmap#troubleshooting-and-debugging)Troubleshooting and Debugging

### [](https://aacle.github.io/nmap#get-help)Get Help

```shell

nmap -h

```

### [](https://aacle.github.io/nmap#display-nmap-version)Display Nmap Version

```shell

nmap -V

```

### [](https://aacle.github.io/nmap#verbose-output)Verbose Output

```shell

nmap -v [target]

```

### [](https://aacle.github.io/nmap#debugging)Debugging

```shell

nmap -d [target]

```

### [](https://aacle.github.io/nmap#display-port-state-reason)Display Port State Reason

```shell

nmap --reason [target]

```

### [](https://aacle.github.io/nmap#only-display-open-ports)Only Display Open Ports

```shell

nmap --open [target]

```

### [](https://aacle.github.io/nmap#trace-packets)Trace Packets

```shell

nmap --packet-trace [target]

```

### [](https://aacle.github.io/nmap#display-host-networking)Display Host Networking

```shell

nmap --iflist

```

### [](https://aacle.github.io/nmap#specify-a-network-interface)Specify a Network Interface

```shell

nmap -e [interface] [target]

```

## [](https://aacle.github.io/nmap#nmap-scripting-engine)Nmap Scripting Engine

### [](https://aacle.github.io/nmap#execute-individual-scripts)Execute Individual Scripts

```shell

nmap --script [script.nse] [target]

```

### [](https://aacle.github.io/nmap#execute-multiple-scripts)Execute Multiple Scripts

```shell

nmap --script [expression] [target]

```

### [](https://aacle.github.io/nmap#execute-scripts-by-category)Execute Scripts by Category

```shell

nmap --script [category] [target]

```

### [](https://aacle.github.io/nmap#execute-multiple-script-categories)Execute Multiple Script Categories

```shell

nmap --script [category1,category2,etc]

```

### [](https://aacle.github.io/nmap#troubleshoot-scripts)Troubleshoot Scripts

```shell

nmap --script [script] --script-trace [target]

```

### [](https://aacle.github.io/nmap#update-the-script-database)Update the Script Database

```shell

nmap --script-updatedb

```

Reference Sites

-   [x]  [Nmap - The Basics](https://www.youtube.com/watch?v=_JvtO-oe8k8)

-   [ ]  [Reference link 1](https://hackertarget.com/nmap-cheatsheet-a-quick-reference-guide/)

-   [ ]  [Beginner's Guide to Nmap](https://www.linux.com/learn/beginners-guide-nmap)

-   [ ]  [Top 32 Nmap Command](https://www.cyberciti.biz/security/nmap-command-examples-tutorials/)

-   [ ]  [Nmap Linux man page](https://linux.die.net/man/1/nmap)

-   [ ]  [29 Practical Examples of Nmap Commands](https://www.tecmint.com/nmap-command-examples/)

-   [ ]  [Nmap Scanning Types, Scanning Commands , NSE Scripts](https://medium.com/@infosecsanyam/nmap-cheat-sheet-nmap-scanning-types-scanning-commands-nse-scripts-868a7bd7f692)

-   [ ]  [Nmap CheatSheet](https://www.cheatography.com/netwrkspider/cheat-sheets/nmap-cheatsheet/)

-   [ ]  [Nmap Cheat Sheet](https://highon.coffee/blog/nmap-cheat-sheet/)

-   [ ]  [Nmap Cheat Sheet: From Discovery to Exploits](https://resources.infosecinstitute.com/nmap-cheat-sheet/)

-   [ ]  [Nmap: my own cheatsheet](https://www.andreafortuna.org/2018/03/12/nmap-my-own-cheatsheet/)

-   [ ]  [NMAP Commands Cheatsheet](https://hackersonlineclub.com/nmap-commands-cheatsheet/)

-   [ ]  [Nmap Cheat Sheet](https://www.stationx.net/nmap-cheat-sheet/)

-   [ ]  [Nmap Cheat Sheet](http://nmapcookbook.blogspot.com/2010/02/nmap-cheat-sheet.html)
