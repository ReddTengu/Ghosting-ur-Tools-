## Feroxbuster Low-Noise Wrapper

A simple Bash wrapper that modifies Feroxbuster's scanning behavior without changing its source code.

### What it does

* Limits the scan to **20 requests/second**.
* Runs the scan for **120 seconds**.
* Preserves Feroxbuster's **state** so recursive scans can resume without starting over.
* Pauses for **7 minutes** after each scan window.
* Automatically resumes the scan after the cooldown.
* Uses --scan-limit 1 to reduce concurrent recursive scans and make the request rate more predictable.

### Workflow

Sending 20 Requests Persecond => 120s scanning => 7min cooldown => resume => repeat


The goal is to reduce aggressive request bursts and make reconnaissance traffic more controlled.
