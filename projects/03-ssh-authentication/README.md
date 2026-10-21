# Correlating SSH Authentication with Captured Network Traffic

**Status:** Observations recorded from an October 15, 2026 lab discussion; verify screenshots and packet capture before treating as evidence-backed.

## Objective
Correlate a network flow in Wireshark with service-side SSH authentication logs in a controlled lab.

## Environment
Windows VM as SSH client and Kali Linux as SSH server, according to the earlier lab walkthrough. The reported private endpoint pair was:

- Client: `10.0.2.15:49334`
- SSH server: `10.0.2.11:22`

IP addresses and ephemeral ports apply only to the historical session and should not be used as general host identities.

## Prior conversation-recorded observations

- Wireshark **TCP stream 107** was associated with the reported SSH flow.
- The Kali service-side log in the walkthrough reported an `Accepted password for kali` event.
- A capture named **`lab01-ssh.pcapng`** was discussed/saved in the earlier lab. **That file is not attached to this portfolio.**
- SSH encrypts the login exchange; successful authentication is supported by the **server log**, not by reading the password from the encrypted packet content.

## Suggested final evidence table (fill using originals)

| Evidence | What to verify | File |
|---|---|---|
| Packet capture | Actual endpoint pair, protocol, stream/timestamps | `lab01-ssh.pcapng` — not included |
| Login log | Correct timestamp, successful event, source IP | Sanitized screenshot — pending |
| Timeline | Match event time to traffic | Pending |

## Limitations and protection
No source log file, screenshot, PCAP file, or synchronized timestamps are included here. Do not publish passwords or private SSH keys. Never imply Wireshark decrypted SSH credentials.

## Interview explanation
“In a controlled SSH lab, I inspected a client/server flow in Wireshark and compared it to an authentication success event in the Kali SSH logs. That helped me distinguish what encrypted network telemetry shows from what the server log confirms.”
