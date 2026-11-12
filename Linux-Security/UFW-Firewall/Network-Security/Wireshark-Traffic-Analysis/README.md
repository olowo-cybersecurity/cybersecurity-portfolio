

# Network Traffic Analysis Using Wireshark

## 1. Project Overview

This project demonstrates the use of Wireshark to capture, monitor and analyse network traffic in a Kali Linux virtual machine running on Oracle VirtualBox.

The project focuses on understanding common network protocols and identifying useful information from captured network packets.

## 2. Objectives

- Capture network traffic using Wireshark.
- Identify DNS, TCP and ICMP protocols.
- Understand the TCP three-way handshake.
- Analyse DNS queries and responses.
- Observe ICMP echo requests and replies.
- Develop basic network monitoring and troubleshooting skills.

## 3. Tools and Environment

| Tool | Purpose |
|---|---|
| Kali Linux | Operating system |
| Oracle VirtualBox | Virtualisation |
| Wireshark | Network traffic analysis |
| Linux Terminal | Generating network traffic |

Network configuration: NAT adapter.

## 4. Methodology

### Step 1: Identify the network interface

Command:

```bash
ip addr
```

This command displays the available network interfaces and their IP addresses.

### Step 2: Launch Wireshark

Command:

```bash
wireshark
```

The active network interface was selected to capture network packets.

### Step 3: Generate DNS traffic

Command:

```bash
nslookup example.com
```

Wireshark display filter:

```text
dns
```

The purpose was to observe DNS queries and responses.

### Step 4: Generate ICMP traffic

Command:

```bash
ping -c 4 8.8.8.8
```

Wireshark display filter:

```text
icmp
```

This exercise was used to observe ICMP echo requests and replies.

### Step 5: Analyse TCP traffic

Command:

```bash
curl -I https://example.com
```

Wireshark display filter:

```text
tcp
```

The following filter was also used to identify initial TCP SYN packets:

```text
tcp.flags.syn == 1 && tcp.flags.ack == 0
```

## 5. Key Concepts

### DNS

DNS translates domain names into IP addresses.

### ICMP

ICMP supports network diagnostics and error reporting. Ping uses ICMP echo requests and replies.

### TCP

TCP provides reliable, connection-oriented communication.

The TCP three-way handshake consists of:

1. SYN
2. SYN-ACK
3. ACK

## 6. Security Relevance

Network traffic analysis helps cybersecurity professionals to:

- Investigate suspicious network communication.
- Identify unusual connection patterns.
- Troubleshoot network connectivity.
- Understand communication between devices.
- Support security monitoring and incident investigations.

## 7. Findings and Observations

This section will contain observations from the actual packet capture.

- DNS observations: [Insert your findings]
- ICMP observations: [Insert your findings]
- TCP observations: [Insert your findings]

## 8. Evidence

Screenshots of the practical exercises will be included in the screenshots folder.

## 9. Conclusion

This project provides practical experience in capturing and analysing network traffic using Wireshark. It demonstrates how DNS, ICMP and TCP protocols can be investigated to understand network communication and support basic cybersecurity monitoring.

## 10. Ethical Considerations

All packet captures were conducted within an authorised personal laboratory environment. No unauthorised network access or interception was performed.

