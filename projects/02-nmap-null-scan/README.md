# Authorized Nmap NULL Scan — Interpreting Uncertain Port States

**Status:** Historical command and output recorded in prior conversation; original screenshot and current VM address verification pending.

## Objective
Learn what a TCP NULL scan sends, how a target may respond, and why Nmap's results can be ambiguous.

## Lab scope
An educational Kali/Windows VM network. **Private addresses below are historical observations**, not current targets. Do not reuse without checking and securing permission.

## Previously recorded command and output — August 17, 2026

```bash
sudo nmap -sN -Pn -p 22 10.0.2.15
```

The earlier discussion recorded Kali at `10.0.2.4` and target `10.0.2.15`, with output resembling:

```text
22/tcp open|filtered ssh
```

A corresponding Wireshark inspection on `eth1` was discussed: a NULL scan sends TCP probe packets with no TCP flag bits set, and a lack of a response was observed in that walkthrough. **This is conversation-recorded text, not a reproduced scan or uploaded capture.** The `ssh` column can be Nmap's service-name mapping for TCP/22; it does not by itself prove an SSH server was running.

## Interpretation

- `open|filtered` **does not mean “open.”** Nmap cannot disambiguate an open service from filtering from this particular observation.
- No response can occur because a port is open, filtering intervenes, or the operating system behaves differently from the expected RFC behavior.
- Further assessment requires a separate permitted scan/test and additional evidence.
- **No confirmed vulnerability or exposure is reported here.**

## Evidence needed

- Redacted terminal screenshot of command and output.
- Redacted Wireshark screenshot highlighting NULL-probe flags (and response context).
- Exact test date, VM interface, authorized scope, and target IP confirmed from original evidence.

## Skills demonstrated
Choosing a scan technique and interpreting uncertainty rather than presenting an inconclusive port state as a discovery.
