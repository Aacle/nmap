Reference guide for scanning networks with Nmap.

Table of Contents

1.  [What is Nmap?](https://github.com/Aacle/nmap#what-is-nmap)

2.  [How to Use Nmap](https://github.com/Aacle/nmap#how-to-use-nmap)

    1.  [Command Line](https://github.com/Aacle/nmap#command-line)

3.  [Basic Scanning Techniques](https://github.com/Aacle/nmap#basic-scanning-techniques)

    1.  [Scan a Single Target](https://github.com/Aacle/nmap#scan-a-single-target)

    2.  [Scan Multiple Targets](https://github.com/Aacle/nmap#scan-multiple-targets)

    3.  [Scan a List of Targets](https://github.com/Aacle/nmap#scan-a-list-of-targets)

    4.  [Scan a Range of Hosts](https://github.com/Aacle/nmap#scan-a-range-of-hosts)

    5.  [Scan an Entire Subnet](https://github.com/Aacle/nmap#scan-an-entire-subnet)

    6.  [Scan Random Hosts](https://github.com/Aacle/nmap#scan-random-hosts)

    7.  [Exclude Targets From a Scan](https://github.com/Aacle/nmap#exclude-targets-from-a-scan)

    8.  [Exclude Targets Using a List](https://github.com/Aacle/nmap#exclude-targets-using-a-list)

    9.  [Perform an Aggresive Scan](https://github.com/Aacle/nmap#perform-an-aggressive-scan)

    10.  [Scan an IPv6 Target](https://github.com/Aacle/nmap#scan-an-ipv6-target)

4.  [Port Scanning Options](https://github.com/Aacle/nmap#port-scanning-options)

    1.  [Perform a Fast Scan](https://github.com/Aacle/nmap#perform-a-fast-scan)

    2.  [Scan Specific Ports](https://github.com/Aacle/nmap#scan-specific-ports)

    3.  [Scan Ports by Name](https://github.com/Aacle/nmap#scan-ports-by-name)

    4.  [Scan Ports by Protocol](https://github.com/Aacle/nmap#scan-ports-by-protocol)

    5.  [Scan All Ports](https://github.com/Aacle/nmap#scan-all-ports)

    6.  [Scan Top Ports](https://github.com/Aacle/nmap#scan-top-ports)

    7.  [Perform a Sequential Port Scan](https://github.com/Aacle/nmap#perform-a-sequential-port-scan)

    8.  [Attempt to Guess an Unknown OS](https://github.com/Aacle/nmap#attempt-to-guess-an-unkown-os)

    9.  [Service Version Detection](https://github.com/Aacle/nmap#service-version-detection)

    10.  [Troubleshoot Version Scan](https://github.com/Aacle/nmap#troubleshoot-version-scan)

    11.  [Perform a RPC Scan](https://github.com/Aacle/nmap#perform-a-rpc-scan)

5.  [Discovery Options](https://github.com/Aacle/nmap#discovery-options)

    1.  [Perform a Ping Only Scan](https://github.com/Aacle/nmap#perform-a-ping-only-scan)

    2.  [Do Not Ping](https://github.com/Aacle/nmap#do-not-ping)

    3.  [TCP SYN Ping](https://github.com/Aacle/nmap#tcp-syn-ping)

    4.  [TCP ACK Ping](https://github.com/Aacle/nmap#tcp-ack-ping)

    5.  [UDP Ping](https://github.com/Aacle/nmap#udp-ping)

    6.  [SCTP INIT Ping](https://github.com/Aacle/nmap#sctp-init-ping)

    7.  [ICMP Echo Ping](https://github.com/Aacle/nmap#icmp-echo-ping)

    8.  [ICMP Timestamp Ping](https://github.com/Aacle/nmap#icmp-timestamp-ping)

    9.  [ICMP Address Mask Ping](https://github.com/Aacle/nmap#icmp-address-mask-ping)

    10.  [IP Protocol Ping](https://github.com/Aacle/nmap#ip-protocol-ping)

    11.  [ARP Ping](https://github.com/Aacle/nmap#arp-ping)

    12.  [Traceroute](https://github.com/Aacle/nmap#traceroute)

    13.  [Force Reverse DNS Resolution](https://github.com/Aacle/nmap#force-reverse-dns-resolution)

    14.  [Disable Reverse DNS Resolution](https://github.com/Aacle/nmap#disable-reverse-dns-resolution)

    15.  [Alternative DNS Lookup](https://github.com/Aacle/nmap#alternate-dns-lookup)

    16.  [Manually Specify DNS Server](https://github.com/Aacle/nmap#manually-specify-dns-server)

    17.  [Create a Host List](https://github.com/Aacle/nmap#create-a-host-list)

6.  [Firewall Evasion Techniques](https://github.com/Aacle/nmap#firewall-evasion-techniques)

    1.  [Fragment Packets](https://github.com/Aacle/nmap#fragment-packets)

    2.  [Specify a Specific MTU](https://github.com/Aacle/nmap#specify-a-specify-mtu)

    3.  [Use a Decoy](https://github.com/Aacle/nmap#use-a-decoy)

    4.  [Idle Zombie Scan](https://github.com/Aacle/nmap#idle-zombie-scan)

    5.  [Manually Specify a Source Port](https://github.com/Aacle/nmap#manually-specify-a-source-port)

    6.  [Append Random Data](https://github.com/Aacle/nmap#append-random-data)

    7.  [Randomize Target Scan Order](https://github.com/Aacle/nmap#randomize-target-scan-order)

    8.  [Spoof MAC Address](https://github.com/Aacle/nmap#spoof-mac-address)

    9.  [Send Bad Checksums](https://github.com/Aacle/nmap#send-bad-checksums)

7.  [Advanced Scanning Functions](https://github.com/Aacle/nmap#advanced-scanning-functions)

    1.  [TCP SYN Scan](https://github.com/Aacle/nmap#tcp-syn-scan)

    2.  [TCP Connect Scan](https://github.com/Aacle/nmap#tcp-connect-scan)

    3.  [UDP Scan](https://github.com/Aacle/nmap#udp-scan)

    4.  [TCP NULL Scan](https://github.com/Aacle/nmap#tcp-null-scan)

    5.  [TCP FIN Scan](https://github.com/Aacle/nmap#tcp-fin-scan)

    6.  [Xmas Scan](https://github.com/Aacle/nmap#xmas-scan)

    7.  [TCP ACK Scan](https://github.com/Aacle/nmap#tcp-ack-scan)

    8.  [Custom TCP Scan](https://github.com/Aacle/nmap#custom-tcp-scan)

    9.  [IP Protocol Scan](https://github.com/Aacle/nmap#ip-protocol-scan)

    10.  [Send Raw Ethernet Packets](https://github.com/Aacle/nmap#send-raw-ethernet-packets)

    11.  [Send IP Packets](https://github.com/Aacle/nmap#send-ip-packets)

8.  [Timing Options](https://github.com/Aacle/nmap#timing-options)

    1.  [Timing Templates](https://github.com/Aacle/nmap#timing-templates)

    2.  [Set the Packet TTL](https://github.com/Aacle/nmap#set-the-packet-ttl)

    3.  [Minimum Number of Parallel Operations](https://github.com/Aacle/nmap#minimum-number-of-parallel-operations)

    4.  [Maximum Number of Parallel Operations](https://github.com/Aacle/nmap#maximum-number-of-parallel-operations)

    5.  [Minimum Host Group Size](https://github.com/Aacle/nmap#minimum-host-group-size)

    6.  [Maximum Host Group Size](https://github.com/Aacle/nmap#maximum-host-group-size)

    7.  [Maximum RTT Timeout](https://github.com/Aacle/nmap#maximum-rtt-timeout)

    8.  [Initial RTT TImeout](https://github.com/Aacle/nmap#initial-rtt-timeout)

    9.  [Maximum Number of Retries](https://github.com/Aacle/nmap#maximum-number-of-retries)

    10.  [Host Timeout](https://github.com/Aacle/nmap#host-timeout)

    11.  [Minimum Scan Delay](https://github.com/Aacle/nmap#minimum-scan-delay)

    12.  [Maximum Scan Delay](https://github.com/Aacle/nmap#maximum-scan-delay)

    13.  [Minimum Packet Rate](https://github.com/Aacle/nmap#minimum-packet-rate)

    14.  [Maximum Packet Rate](https://github.com/Aacle/nmap#maximum-packet-rate)

    15.  [Defeat Reset Rate Limits](https://github.com/Aacle/nmap#defeat-reset-rate-limits)

9.  [Output Options](https://github.com/Aacle/nmap#output-options)

    1.  [Save Output to a Text File](https://github.com/Aacle/nmap#save-output-to-a-text-file)

    2.  [Save Output to a XML File](https://github.com/Aacle/nmap#save-output-to-a-xml-file)

    3.  [Grepable Output](https://github.com/Aacle/nmap#grepable-output)

    4.  [Output All Supported File Types](https://github.com/Aacle/nmap#output-all-supported-file-types)

    5.  [Periodically Display Statistics](https://github.com/Aacle/nmap#periodically-display-statistics)

    6.  [1337 Output](https://github.com/Aacle/nmap#1337-output)

10.  [Compare Scans](https://github.com/Aacle/nmap#compare-scans)

    1.  [Comparison Using Ndiff](https://github.com/Aacle/nmap#comparison-using-ndiff)

    2.  [Ndiff Verbose Mode](https://github.com/Aacle/nmap#ndiff-verbose-mode)

    3.  [XML Output Mode](https://github.com/Aacle/nmap#xml-output-mode)

11.  [Troubleshooting and Debugging](https://github.com/Aacle/nmap#troubleshooting-and-debugging)

    1.  [Get Help](https://github.com/Aacle/nmap#get-help)

    2.  [Display Nmap Version](https://github.com/Aacle/nmap#display-nmap-version)

    3.  [Verbose Output](https://github.com/Aacle/nmap#verbose-output)

    4.  [Debugging](https://github.com/Aacle/nmap#debugging)

    5.  [Display Port State Reason](https://github.com/Aacle/nmap#display-port-state-reason)

    6.  [Only Display Open Ports](https://github.com/Aacle/nmap#only-display-open-ports)

    7.  [Trace Packets](https://github.com/Aacle/nmap#trace-packets)

    8.  [Display Host Networking](https://github.com/Aacle/nmap#display-host-networking)

    9.  [Specify a Network Interface](https://github.com/Aacle/nmap#specify-a-network-interface)

12.  Nmap Scripting Engine

    1.  [Execute Individual Scripts](https://github.com/Aacle/nmap#execute-individual-scripts)

    2.  [Execute Multiple Scripts](https://github.com/Aacle/nmap#execute-multiple-scripts)

    3.  [Execute Scripts by Category](https://github.com/Aacle/nmap#execute-scripts-by-category)

    4.  [Execute Multiple Script Categories](https://github.com/Aacle/nmap#execute-multiple-script-categories)

    5.  [Troubleshoot Scripts](https://github.com/Aacle/nmap#troubleshoot-scripts)

    6.  [Update the Script Database](https://github.com/Aacle/nmap#update-the-script-database)

## [](https://github.com/Aacle/nmap#what-is-nmap)What is Nmap?

Nmap ("Network Mapper") is a free and open source utility for network discovery and security auditing. Many systems and network administrators also find it useful for tasks such as network inventory, managing service upgrade schedules, and monitoring host or service uptime. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running. It was designed to rapidly scan large networks, but works fine against single hosts.

## [](https://github.com/Aacle/nmap#how-to-use-nmap)How to Use Nmap

Nmap can be used in a variety of ways depending on the user's level of technical expertise.

| Technical Expertise | Usage |

| :-- | :-- |

| Beginner | [Zenmap](https://nmap.org/zenmap/) the graphical user interface for Nmap |

| Intermediate | [Command line](https://nmap.org/) |

| Advanced | Python scripting with the [Python-Nmap](https://pypi.org/project/python-nmap/) package |

### [](https://github.com/Aacle/nmap#command-line)Command Line

```shell

nmap [ <Scan Type> ...] [ <Options> ] { <target specification> }

```

## [](https://github.com/Aacle/nmap#basic-scanning-techniques)Basic Scanning Techniques

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

### [](https://github.com/Aacle/nmap#scan-a-single-target)Scan a Single Target

```shell

nmap [target]

```

### [](https://github.com/Aacle/nmap#scan-multiple-targets)Scan Multiple Targets

```shell

nmap [target1, target2, etc]

```

### [](https://github.com/Aacle/nmap#scan-a-list-of-targets)Scan a List of Targets

```shell

nmap -iL [list.txt]

```

### [](https://github.com/Aacle/nmap#scan-a-range-of-hosts)Scan a Range of Hosts

```shell

nmap [range of IP addresses]

```

### [](https://github.com/Aacle/nmap#scan-an-entire-subnet)Scan an Entire Subnet

```shell

nmap [ip address/cdir]

```

### [](https://github.com/Aacle/nmap#scan-random-hosts)Scan Random Hosts

```shell

nmap -iR [number]

```

### [](https://github.com/Aacle/nmap#exclude-targets-from-a-scan)Exclude Targets From a Scan

```shell

nmap [targets] --exclude [targets]

```

### [](https://github.com/Aacle/nmap#exclude-targets-using-a-list)Exclude Targets Using a List

```shell

nmap [targets] --excludefile [list.txt]

```

### [](https://github.com/Aacle/nmap#perform-an-aggresive-scan)Perform an Aggresive Scan

```shell

nmap -A [target]

```

### [](https://github.com/Aacle/nmap#scan-an-ipv6-target)Scan an IPv6 Target

```shell

nmap -6 [target]

```

## [](https://github.com/Aacle/nmap#port-scanning-options)Port Scanning Options

### [](https://github.com/Aacle/nmap#perform-a-fast-scan)Perform a Fast Scan

```shell

nmap -F [target]

```

### [](https://github.com/Aacle/nmap#scan-specific-ports)Scan Specific Ports

```shell

nmap -p [port(s)] [target]

```

### [](https://github.com/Aacle/nmap#scan-ports-by-name)Scan Ports by Name

```shell

nmap -p [port name(s)] [target]

```

### [](https://github.com/Aacle/nmap#scan-ports-by-protocol)Scan Ports by Protocol

```shell

nmap -sU -sT -p U:[ports],T:[ports] [target]

```

### [](https://github.com/Aacle/nmap#scan-all-ports)Scan All Ports

```shell

nmap -p 1-65535 [target]

```

### [](https://github.com/Aacle/nmap#scan-top-ports)Scan Top Ports

```shell

nmap --top-ports [number] [target]

```

### [](https://github.com/Aacle/nmap#perform-a-sequential-port-scan)Perform a Sequential Port Scan

```shell

nmap -r [target]

```

### [](https://github.com/Aacle/nmap#attempt-to-guess-an-unknown-os)Attempt to Guess an Unknown OS

```shell

nmap -O --osscan-guess [target]

```

### [](https://github.com/Aacle/nmap#service-version-detection)Service Version Detection

```shell

nmap -sV [target]

```

### [](https://github.com/Aacle/nmap#troubleshoot-version-scan)Troubleshoot Version Scan

```shell

nmap -sV --version-trace [target]

```

### [](https://github.com/Aacle/nmap#perform-a-rpc-scan)Perform a RPC Scan

```shell

nmap -sR [target]

```

## [](https://github.com/Aacle/nmap#discovery-options)Discovery Options

Host Discovery The `-p` switch determines the type of ping to perform.

| Nmap Switch | Description |

| :-- | :-- |

| \-PI | ICMP ping |

| \-Po | No ping |

| \-PS | SYN ping |

| \-PT | TCP ping |

### [](https://github.com/Aacle/nmap#perform-a-ping-only-scan)Perform a Ping Only Scan

```shell

nmap -sn [target]

```

### [](https://github.com/Aacle/nmap#do-not-ping)Do Not Ping

```shell

nmap -Pn [target]

```

### [](https://github.com/Aacle/nmap#tcp-syn-ping)TCP SYN Ping

```shell

nmap -PS [target]

```

### [](https://github.com/Aacle/nmap#tcp-ack-ping)TCP ACK Ping

```shell

nmap -PA [target]

```

### [](https://github.com/Aacle/nmap#udp-ping)UDP Ping

```shell

nmap -PU [target]

```

### [](https://github.com/Aacle/nmap#sctp-init-ping)SCTP INIT Ping

```shell

nmap -PY [target]

```

### [](https://github.com/Aacle/nmap#icmp-echo-ping)ICMP Echo Ping

```shell

nmap -PE [target]

```

### [](https://github.com/Aacle/nmap#icmp-timestamp-ping)ICMP Timestamp Ping

```shell

nmap -PP [target]

```

### [](https://github.com/Aacle/nmap#icmp-address-mask-ping)ICMP Address Mask Ping

```shell

nmap -PM [target]

```

### [](https://github.com/Aacle/nmap#ip-protocol-ping)IP Protocol Ping

```shell

nmap -PO [target]

```

### [](https://github.com/Aacle/nmap#arp-ping)ARP ping

```shell

nmap -PR [target]

```

### [](https://github.com/Aacle/nmap#traceroute)Traceroute

```shell

nmap --traceroute [target]

```

### [](https://github.com/Aacle/nmap#force-reverse-dns-resolution)Force Reverse DNS Resolution

```shell

nmap -R [target]

```

### [](https://github.com/Aacle/nmap#disable-reverse-dns-resolution)Disable Reverse DNS Resolution

```shell

nmap -n [target]

```

### [](https://github.com/Aacle/nmap#alternative-dns-lookup)Alternative DNS Lookup

```shell

nmap --system-dns [target]

```

### [](https://github.com/Aacle/nmap#manually-specify-dns-server)Manually Specify DNS Server

Can specify a single server or multiple.

```shell

nmap --dns-servers [servers] [target]

```

### [](https://github.com/Aacle/nmap#create-a-host-list)Create a Host List

```shell

nmap -sL [targets]

```

## [](https://github.com/Aacle/nmap#port-specification-and-scan-order)Port Specification and Scan Order

| Nmap Switch | Description |

| :-- | :-- |

## [](https://github.com/Aacle/nmap#serviceversion-detection)Service/Version Detection

| Nmap Switch | Description |

| :-- | :-- |

| \-sV | Enumerates software versions |

## [](https://github.com/Aacle/nmap#script-scan)Script Scan

| Nmap Switch | Description |

| :-- | :-- |

| \-sC | Run all default scripts |

## [](https://github.com/Aacle/nmap#os-detection)OS Detection

| Nmap Switch | Description |

| :-- | :-- |

## [](https://github.com/Aacle/nmap#timing-and-performance)Timing and Performance

The `-t` switch determines the speed and stealth performed.

| Nmap Switch | Description |

| :-- | :-- |

| \-T0 | Serial, slowest scan |

| \-T1 | Serial, slow scan |

| \-T2 | Serial, normal speed scan |

| \-T3 | Parallel, normal speed scan |

| \-T4 | Parallel, fast scan |

Not specifying a `T` value will default to `-T3`, or normal speed.

## [](https://github.com/Aacle/nmap#firewall-evasion-techniques)Firewall Evasion Techniques

### [](https://github.com/Aacle/nmap#firewallids-evasion-and-spoofing)Firewall/IDS Evasion and Spoofing

| Nmap Switch | Description |

| :-- | :-- |

### [](https://github.com/Aacle/nmap#fragment-packets)Fragment Packets

```shell

nmap -f [target]

```

### [](https://github.com/Aacle/nmap#specify-a-specific-mtu)Specify a Specific MTU

```shell

nmap --mtu [MTU] [target]

```

### [](https://github.com/Aacle/nmap#use-a-decoy)Use a Decoy

```shell

nmap -D RND:[number] [target]

```

### [](https://github.com/Aacle/nmap#idle-zombie-scan)Idle Zombie Scan

```shell

nmap -sI [zombie] [target]

```

### [](https://github.com/Aacle/nmap#manually-specify-a-source-port)Manually Specify a Source Port

```shell

nmap --source-port [port] [target]

```

### [](https://github.com/Aacle/nmap#append-random-data)Append Random Data

```shell

nmap --data-length [size] [target]

```

### [](https://github.com/Aacle/nmap#randomize-target-scan-order)Randomize Target Scan Order

```shell

nmap --randomize-hosts [target]

```

### [](https://github.com/Aacle/nmap#spoof-mac-address)Spoof MAC Address

```shell

nmap --spoof-mac [MAC|0|vendor] [target]

```

### [](https://github.com/Aacle/nmap#send-bad-checksums)Send Bad Checksums

```shell

nmap --badsum [target]

```

## [](https://github.com/Aacle/nmap#advanced-scanning-functions)Advanced Scanning Functions

### [](https://github.com/Aacle/nmap#tcp-syn-scan)TCP SYN Scan

```shell

nmap -sS [target]

```

### [](https://github.com/Aacle/nmap#tcp-connect-scan)TCP Connect Scan

    nmap -sT [target]

    

### [](https://github.com/Aacle/nmap#udp-scan)UDP Scan

```shell

nmap -sU [target]

```

### [](https://github.com/Aacle/nmap#tcp-null-scan)TCP NULL Scan

```shell

nmap -sN [target]

```

### [](https://github.com/Aacle/nmap#tcp-fin-scan)TCP FIN Scan

```shell

nmap -sF [target]

```

### [](https://github.com/Aacle/nmap#xmas-scan)Xmas Scan

```shell

nmap -sA [target]

```

### [](https://github.com/Aacle/nmap#tcp-ack-scan)TCP ACK Scan

```shell

nmap -sA [target]

```

### [](https://github.com/Aacle/nmap#custom-tcp-scan)Custom TCP Scan

```shell

nmap --scanflags [flags] [target]

```

### [](https://github.com/Aacle/nmap#ip-protocol-scan)IP Protocol Scan

```shell

nmap -sO [target]

```

### [](https://github.com/Aacle/nmap#send-raw-ethernet-packets)Send Raw Ethernet Packets

```shell

nmap --send-eth [target]

```

### [](https://github.com/Aacle/nmap#send-ip-packets)Send IP Packets

```shell

nmap --send-ip [target]

```

## [](https://github.com/Aacle/nmap#timing-options)Timing Options

### [](https://github.com/Aacle/nmap#timing-templates)Timing Templates

```shell

nmap -T[0-5] [target]

```

### [](https://github.com/Aacle/nmap#set-the-packet-ttl)Set the Packet TTL

```shell

nmap --ttl [time] [target]

```

### [](https://github.com/Aacle/nmap#minimum-number-of-parallel-operations)Minimum NUmber of Parallel Operations

```shell

nmap --min-parallelism [number] [target]

```

### [](https://github.com/Aacle/nmap#maximum-number-of-parallel-operations)Maximum Number of Parallel Operations

```shell

nmap --max-parallelism [number] [target]

```

### [](https://github.com/Aacle/nmap#minimum-host-group-size)Minimum Host Group Size

```shell

nmap --min-hostgroup [number] [targets]

```

### [](https://github.com/Aacle/nmap#maximum-host-group-size)Maximum Host Group Size

```shell

nmap --max-hostgroup [number] [targets]

```

### [](https://github.com/Aacle/nmap#maximum-rtt-timeout)Maximum RTT Timeout

```shell

nmap --initial-rtt-timeout [time] [target]

```

### [](https://github.com/Aacle/nmap#initial-rtt-timeout)Initial RTT Timeout

```shell

nmap --max-rtt-timeout [TTL] [target]

```

### [](https://github.com/Aacle/nmap#maximum-number-of-retries)Maximum Number of Retries

```shell

nmap --max-retries [number] [target]

```

### [](https://github.com/Aacle/nmap#host-timeout)Host Timeout

```shell

nmap --host-timeout [time] [target]

```

### [](https://github.com/Aacle/nmap#minimum-scan-delay)Minimum Scan Delay

```shell

nmap --scan-delay [time] [target]

```

### [](https://github.com/Aacle/nmap#maxmimum-scan-delay)Maxmimum Scan Delay

```shell

nmap --max-scan-delay [time] [target]

```

### [](https://github.com/Aacle/nmap#minimum-packet-rate)Minimum Packet Rate

```shell

nmap --min-rate [number] [target]

```

### [](https://github.com/Aacle/nmap#maximum-packet-rate)Maximum Packet Rate

```shell

nmap --max-rate [number] [target]

```

### [](https://github.com/Aacle/nmap#defeat-reset-rate-limits)Defeat Reset Rate Limits

```shell

nmap --defeat-rst-ratelimit [target]

```

## [](https://github.com/Aacle/nmap#output-options)Output Options

| Nmap Switch | Description |

| :-- | :-- |

| `-oN` | Normal output |

| `-oX` | XML output |

| `-oA` | Normal, XML, and Grepable format all at once |

### [](https://github.com/Aacle/nmap#save-output-to-a-text-file)Save Output to a Text File

```shell

nmap -oN [scan.txt] [target]

```

### [](https://github.com/Aacle/nmap#save-output-to-a-xml-file)Save Output to a XML File

```shell

nmap -oX [scan.xml] [target]

```

### [](https://github.com/Aacle/nmap#grepable-output)Grepable Output

```shell

nmap -oG [scan.txt] [target]

```

### [](https://github.com/Aacle/nmap#output-all-supported-file-types)Output All Supported File Types

```shell

nmap -oA [path/filename] [target]

```

### [](https://github.com/Aacle/nmap#periodically-display-statistics)Periodically Display Statistics

```shell

nmap --stats-every [time] [target]

```

### [](https://github.com/Aacle/nmap#1337-output)1337 Output

```shell

nmap -oS [scan.txt] [target]

```

## [](https://github.com/Aacle/nmap#compare-scans)Compare Scans

### [](https://github.com/Aacle/nmap#comparison-using-ndiff)Comparison Using Ndiff

```shell

ndiff [scan1.xml] [scan2.xml]

```

### [](https://github.com/Aacle/nmap#ndiff-verbose-mode)Ndiff Verbose Mode

```shell

ndiff -v [scan1.xml] [scan2.xml]

```

### [](https://github.com/Aacle/nmap#xml-output-mode)XML Output Mode

```shell

ndiff --xml [scan1.xml] [scan2.xml]

```

## [](https://github.com/Aacle/nmap#troubleshooting-and-debugging)Troubleshooting and Debugging

### [](https://github.com/Aacle/nmap#get-help)Get Help

```shell

nmap -h

```

### [](https://github.com/Aacle/nmap#display-nmap-version)Display Nmap Version

```shell

nmap -V

```

### [](https://github.com/Aacle/nmap#verbose-output)Verbose Output

```shell

nmap -v [target]

```

### [](https://github.com/Aacle/nmap#debugging)Debugging

```shell

nmap -d [target]

```

### [](https://github.com/Aacle/nmap#display-port-state-reason)Display Port State Reason

```shell

nmap --reason [target]

```

### [](https://github.com/Aacle/nmap#only-display-open-ports)Only Display Open Ports

```shell

nmap --open [target]

```

### [](https://github.com/Aacle/nmap#trace-packets)Trace Packets

```shell

nmap --packet-trace [target]

```

### [](https://github.com/Aacle/nmap#display-host-networking)Display Host Networking

```shell

nmap --iflist

```

### [](https://github.com/Aacle/nmap#specify-a-network-interface)Specify a Network Interface

```shell

nmap -e [interface] [target]

```

## [](https://github.com/Aacle/nmap#nmap-scripting-engine)Nmap Scripting Engine

### [](https://github.com/Aacle/nmap#execute-individual-scripts)Execute Individual Scripts

```shell

nmap --script [script.nse] [target]

```

### [](https://github.com/Aacle/nmap#execute-multiple-scripts)Execute Multiple Scripts

```shell

nmap --script [expression] [target]

```

### [](https://github.com/Aacle/nmap#execute-scripts-by-category)Execute Scripts by Category

```shell

nmap --script [category] [target]

```

### [](https://github.com/Aacle/nmap#execute-multiple-script-categories)Execute Multiple Script Categories

```shell

nmap --script [category1,category2,etc]

```

### [](https://github.com/Aacle/nmap#troubleshoot-scripts)Troubleshoot Scripts

```shell

nmap --script [script] --script-trace [target]

```

### [](https://github.com/Aacle/nmap#update-the-script-database)Update the Script Database

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
