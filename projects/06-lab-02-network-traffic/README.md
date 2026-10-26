# Lab 2 — Network Traffic Investigation (Walkthrough)

**Status:** Documentation in progress — evidence and commands pending verification  
**Environment:** Authorized Kali Linux virtual-machine training lab

## Purpose
Document the lab as a reproducible investigation: not just the result, but **how each piece of evidence was obtained, what it shows, and what conclusions are justified**.

## Observations recalled from our Lab 2 session
The following are notes from our discussion, **not independently verified against uploaded packet captures or screenshots**:

- The Kali VM's recorded IP address was `10.0.2.15`.
- The recorded default gateway was `10.0.2.1`.
- A Wireshark HTTP exercise showed request/response traffic with `200 OK` results.
- We examined whether the client IP was consistent across the observed exchange.

A `200 OK` HTTP response indicates success for that request. It **does not by itself prove** that a server is secure or that a vulnerability exists. The client and gateway addresses are historical lab observations and should be checked against the evidence before finalizing this project.

## Walkthrough and evidence

### Step 1 — Establish the lab environment
**Question:** Which VM and network adapter were used?  
**Command or action:** *To be reconstructed from the lab screenshot or notes.*  
**Evidence:** *Pending: screenshot showing the Kali IP and gateway.*  
**Analysis:** Confirm the source IP and default gateway, and distinguish them from any target/server addresses.

### Step 2 — Start and capture network traffic
**Question:** Which network interface was captured, and what traffic was generated?  
**Command or action:** *Pending verification.*  
**Evidence:** *Pending: Wireshark capture overview and display filter.*  
**Analysis:** Identify the capture interface, endpoints, and protocol without inventing packet details.

### Step 3 — Inspect the HTTP request
**Question:** Which client sent the HTTP request, to which server, and for what resource?  
**Command or action:** *Pending verification.*  
**Evidence:** *Pending: screenshot of selected HTTP request and packet details.*  
**Analysis:** Record source/destination IP, method, host, URI, and packet number **only if visible**.

### Step 4 — Inspect the HTTP response
**Question:** What did the server return?  
**Command or action:** *Pending verification.*  
**Evidence:** *Pending: screenshot of `200 OK` response and related request.*  
**Analysis:** Explain what the response code confirms and what it cannot establish.

### Step 5 — Correlate the conversation
**Question:** Do the request and response belong to the same client-server exchange?  
**Command or action:** *Pending verification (e.g., Follow TCP Stream if shown).*  
**Evidence:** *Pending: correlated packets or TCP stream screenshot.*  
**Analysis:** Check IP addresses, ports, stream identifiers, and sequence of events before making a conclusion.

## Evidence inventory
| ID | Evidence file | What it should verify | Status |
|---|---|---|---|
| E01 | `evidence/01-network-configuration.png` | VM address and gateway | Not uploaded |
| E02 | `evidence/02-capture-overview.png` | Wireshark interface and traffic | Not uploaded |
| E03 | `evidence/03-http-request.png` | HTTP request details | Not uploaded |
| E04 | `evidence/04-http-response.png` | HTTP 200 response | Not uploaded |
| E05 | `evidence/05-conversation-analysis.png` | Request/response correlation | Not uploaded |

*File names are proposed placeholders, not claims that evidence exists.*

## Findings
**Provisional:** The training traffic included at least one successful HTTP response. Stronger findings will be added only after reviewing the original evidence.

## Limitations
- The exact lab instructions, executed commands, packet capture, and screenshots have not yet been attached to this project.
- No vulnerability, compromise, or unauthorized activity is claimed.

## Next steps
1. Upload the Lab 2 screenshots in chronological order.
2. Compare each screenshot to the lab instructions and reconstruct the action taken.
3. Fill in the command/action, observation, interpretation, and supporting screenshot for each step.
4. Recheck all addresses, response codes, filters, and conclusions.
5. Finish with a defensible incident-style summary suitable for a job interview.
