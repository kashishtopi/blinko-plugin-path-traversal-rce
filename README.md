# Blinko: Authenticated Plugin Path Traversal to Root Code Execution

CVE pending (reserved).

Any authenticated Blinko user can abuse the plugin installer's unsanitized `name` value to
write files outside the plugins directory. The official image runs as root, so overwriting a
root-owned startup file gives remote code execution as root.

- Affected: Blinko 1.8.8 and earlier
- CWE-22 (Path Traversal)
- CVSS 3.1: 9.9 Critical (AV:N/AC:L/PR:L/UI:N/S:C/C:H/I:H/A:H)

Full write-up and proof of concept: **[HR-blinko-plugin-path-traversal-rce.pdf](HR-blinko-plugin-path-traversal-rce.pdf)**

## Disclaimer

This proof of concept is for authorized security testing and education only.
Test only systems that you own or have explicit permission to test. The author
takes no responsibility for misuse.
