# Wireshark HTTP Response and TCP Stream Analysis

**Status:** Practical observations previously discussed; screenshots/PCAP not yet attached or independently verified.

## Objective
Explain how packet captures show a web client request, the server response, and the TCP conversation that transports them.

## Environment and tools
Wireshark, a browser, and an educational HTTP traffic trace / controlled lab activity. Previous lab material also referenced the UMass HTTP Wireshark exercise. **Do not assume a particular capture is the user's own traffic unless its origin is verified.**

## Conversation-recorded observations

- In October 2026, the analyst used Wireshark to inspect a TCP conversation and used **Follow TCP Stream**.
- A prior session discussed an **HTTP `200 OK`** server response, which means the particular HTTP request succeeded at the application-protocol level; it does not mean the system is secure.
- Screenshots were shared in earlier chats, but the **actual image files and original `.pcapng` have not been recovered** for this portfolio.

## Analysis workflow (illustrative, not an audited command log)

1. Inspect packet list and confirm client/server IP addresses from the **actual** trace.
2. Filter relevant traffic, e.g. `http` or `tcp.stream == <stream-number>`.
3. Locate request and response in the packet details; record the request method, URI and HTTP status code from the trace.
4. Use **Follow > TCP Stream** to distinguish client and server payloads.
5. Record frame number, timestamps, status, and relevant TCP flags from the real capture.
6. Compare evidence with the exercise questions and describe limitations.

## Finding summary
An earlier lab walkthrough reached a readable HTTP response and a followed TCP stream. **The packet numbers, request path, host details, and screenshot-backed conclusions are pending verification.** No malicious activity or vulnerability is claimed.

## Evidence to add

- `evidence/01-http-response-redacted.png`: an original image showing HTTP `200 OK` or the relevant packet detail.
- `evidence/02-follow-tcp-stream-redacted.png`: a sanitized original Follow TCP Stream view.
- Optional sanitized `*.pcapng` (only if it contains no private traffic or credentials); otherwise retain it privately and describe the evidence.

## Interview explanation
“I used Wireshark to inspect an HTTP response and followed the TCP stream to understand the request/response exchange. I documented the response behavior and can explain the difference between transport-layer packets and application-layer content.”

## Next verification step
Open the original capture or upload the earlier screenshots, note the exact response packet and stream number, and update this report with an evidence table.
