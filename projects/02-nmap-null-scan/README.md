# Nmap Network Security Assessment

## Project Overview

Conducted a TCP NULL scan in an authorized virtual-machine training environment using Nmap.

The objective was to investigate TCP port behavior, interpret scan results, and understand the limitations of network reconnaissance.

## Tools Used

- Nmap
- Kali Linux
- Virtual-machine networking
- TCP/IP

## Investigation Objectives

1. Perform an authorized network scan.
2. Examine TCP port states.
3. Understand how TCP NULL scans work.
4. Interpret ambiguous scan results.
5. Document findings accurately.

## Lab Activity

Used Nmap's `-sN` option to perform a TCP NULL scan against a training VM.

A NULL scan sends TCP probes with no TCP flags set.

The lab included examining results reported as `open|filtered`.

## Findings

### Open or Filtered Ports

Nmap reported an `open|filtered` state during the exercise.

This result means Nmap could not determine whether the port was open or whether traffic was being filtered.

An `open|filtered` result does not confirm an active service or a vulnerability.

### Technical Interpretation

TCP NULL scans can help investigate how a system responds to unusual TCP probes.

Results may vary depending on the operating system, firewall configuration, and network conditions.

Additional authorized testing would be necessary to determine the actual state of an ambiguous port.

## Screenshot Evidence

[View Nmap NULL Scan Results](evidence/nmap%20download.png)

## Skills Demonstrated

- Network reconnaissance
- TCP port-state interpretation
- Nmap command-line usage
- Security assessment fundamentals
- Technical documentation
- Understanding scan limitations

## Conclusion

This training exercise improved my understanding of TCP scanning techniques and the importance of interpreting network-security results accurately.

The screenshot documents an educational lab exercise. No confirmed vulnerability or unauthorized assessment is claimed.
