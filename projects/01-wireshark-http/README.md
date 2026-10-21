# Wireshark HTTP Traffic Analysis

## Project Overview

Investigated HTTP network traffic using Wireshark in an educational lab environment. Examined client-server communication, TCP streams, HTTP response codes, and server headers.

## Tools Used

- Wireshark
- TCP/IP
- HTTP
- Kali Linux lab environment
- UMass HTTP Wireshark training exercise

## Investigation Objectives

1. Identify HTTP requests and responses.
2. Inspect communication between client and server.
3. Use Follow TCP Stream to examine HTTP conversations.
4. Interpret HTTP response codes and headers.
5. Document packet-level observations.

## Findings

### HTTP 200 OK

Observed a successful HTTP response from a web server.

- Client IP: 10.0.2.11
- Server IP: 128.119.245.12
- HTTP status: 200 OK
- Server header: Apache/2.4.62 (AlmaLinux)
- Content type: text/html

Used Wireshark's Follow TCP Stream feature to inspect the HTTP request and response.

### HTTP 304 Not Modified

Examined HTTP caching behavior and the meaning of a 304 response, which indicates that the requested representation has not changed under the applicable conditional request.

### Technical Interpretation

An HTTP 200 response confirms that a particular HTTP request succeeded. It does not, by itself, establish whether a system is secure.

A 304 response demonstrates conditional HTTP request behavior and can help explain browser caching.

## Screenshot Evidence

- [HTTP 200 and Follow TCP Stream](evidence/Screenshot%202026-10-16%20150146.png)
- [HTTP 304 Not Modified](evidence/02-http-304-not-modified.png)
- [Additional HTTP 200 Response Analysis](evidence/03-http-200-curl-response.png)

## Skills Demonstrated

- Network packet analysis
- TCP stream inspection
- HTTP request and response analysis
- Protocol troubleshooting
- Technical documentation

## Conclusion

This guided lab improved my ability to investigate network communication using Wireshark, interpret HTTP responses, and document observable network behavior.

The screenshots are from a training environment. No real-world intrusion or vulnerability is claimed.
