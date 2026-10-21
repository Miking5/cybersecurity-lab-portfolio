# Digital Forensics: Scalpel File-Carving Troubleshooting

**Status: Incomplete.** Do **not** describe this as successful file recovery.

## Objective
Practice carving known file types from an authorized forensic image and documenting reproducible results.

## Conversation-recorded activity

- Reviewed a file-carving lab guide and worked with Kali/Scalpel configuration and command-line paths.
- A September 16, 2026 lab troubleshooting session could not find the expected image (`windows7_64GB_image.dd`) under `/home/kali`. Searches did not locate the required practice evidence there.
- Therefore the investigation **did not establish recovered JPEG/PDF/Excel artifacts** from that image.

## Workflow to complete later

1. Confirm which forensic image the lab authorizes and where it is actually stored.
2. Record its hash and keep the source read-only.
3. Confirm `scalpel.conf` file signatures are enabled for desired types.
4. Run Scalpel against the authorized image and a separate output folder.
5. Verify recovered files with appropriate file identification and document each outcome, including false positives.

## Current finding
The immediate blocker was an **unavailable input forensic image**, not a verified recovery result. Troubleshooting the evidence path is part of sound investigative practice.

## Evidence needed
Original command-line images, the authorized input image path/hash, audit trail, output directory contents, and screenshots of files only if legitimately recovered.
