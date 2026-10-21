# Volatility 3 Memory Analysis — Partial Windows Triage

**Status:** **In progress / partial findings**. Original memory image and screenshots unavailable in this repository.

## Objective
Explore processes and network artifacts in a Windows lab memory image using Volatility 3.

## Activity from previous lab conversations

- Set up and launched Volatility 3 in Kali (`/opt/volatility3` was mentioned during troubleshooting).
- A September 24, 2026 walkthrough described output including `explorer.exe`, `chrome.exe`, `cmd.exe`, `conhost.exe`, and `MRCv120.exe`.
- An earlier `windows.netscan` discussion identified `172.16.0.5:139 LISTENING`, PID 4, shown as `System` in the output.
- Other attempts ran into tool/image problems or crashes. These findings are **not enough to conclude compromise**.

## Example commands to document after verification

```bash
# Examples of syntax, not claims that each command succeeded
python3 vol.py -f <your-authorized-memory-image> windows.info
python3 vol.py -f <your-authorized-memory-image> windows.pslist
python3 vol.py -f <your-authorized-memory-image> windows.netscan
```

## Cautions
An executable process name does not establish malware, and listening on SMB/NetBIOS TCP 139 is not inherently malicious. Re-open the original memory image and capture precise output/screenshots before refining these findings.

## Evidence to add
Authorized memory-image provenance (not the dump itself on a public repo), command/output screenshots, operating system details, plugin versions, hash if collected, timestamps and errors.
