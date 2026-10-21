# SSH Authentication and Network Traffic Investigation

## Project Overview

Investigated SSH network communication and authentication activity in a controlled cybersecurity lab.

Used Wireshark to examine encrypted SSH traffic and Kali Linux authentication logs to understand how network and host-based evidence complement each other.

## Tools Used

- Wireshark
- Kali Linux
- Windows virtual machine
- SSH (Secure Shell)
- Linux authentication logs
- TCP/IP

## Investigation Objectives

1. Identify SSH network connections.
2. Examine TCP port 22 traffic.
3. Inspect SSH protocol and connection activity.
4. Review server-side authentication events.
5. Compare network observations with system logs.

## Lab Environment

- SSH client: Windows VM
- SSH server: Kali Linux
- Protocol: SSH over TCP
- Server port: 22

Historical lab observations included:

- Client: `10.0.2.15`
- Server: `10.0.2.11`
- Wireshark TCP stream: 107

These addresses and stream numbers apply only to the recorded training exercise.

## Investigation Findings

### 1. SSH Network Traffic

Examined SSH communication using Wireshark.

The capture demonstrated a network connection involving TCP port 22 and SSH protocol activity.

SSH encrypts application data, so the packet capture does not reveal plaintext login credentials.

### 2. Authentication Log Investigation

Reviewed SSH authentication events recorded by the Kali Linux system.

The earlier lab investigation included an `Accepted password for kali` event, indicating that the SSH server accepted a password-based authentication attempt.

This authentication result comes from server-side logging, not decrypted Wireshark traffic.

### 3. Evidence Correlation

Compared observations from network traffic with SSH authentication records.

The exercise demonstrated why security analysts investigate multiple evidence sources when determining what occurred during a connection.

Exact timestamp correlation remains to be verified from the original capture and logs.

## Screenshot Evidence

- [SSH Traffic and Protocol Analysis](evidence/01-ssh-handshake-wireshark.png)
- [SSH Authentication Log Investigation](evidence/02-ssh-authentication-journal.png)

## Skills Demonstrated

- Network traffic investigation
- TCP/IP and SSH protocol analysis
- Linux authentication-log review
- Wireshark packet inspection
- Security-event investigation
- Technical documentation

## Conclusion

This lab strengthened my ability to investigate SSH activity using both network-based and host-based evidence.

It demonstrated the importance of distinguishing encrypted network communication from authentication events confirmed by server logs.

The screenshots document training activity. The original packet capture and raw logs are not published, and no malicious intrusion is claimed.
