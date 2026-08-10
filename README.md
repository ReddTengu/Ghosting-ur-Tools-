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

___________________________________________________________________

# 👾Editing Simple Tools With Simple Code👾!

I'm trying to edit the tools that I use to work against targets that use security systems such as WAFs, IDS/IPS, and firewalls.

I've studied Blue Team tactics to discover how attackers are detected and how firewalls, WAFs, and IDS/IPS are configured to detect attackers through patterns such as a high volume of requests in a short period of time, sustained request volumes over a longer period, aggressive scans, etc.

My goal is to perform my reconnaissance process without the headache of triggering security systems.

I'm mainly focusing on web penetration testing now, so I'll only work on tools related to web penetration testing.
