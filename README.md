# Description

A simple Bash wrapper that modifies Feroxbuster's scanning behavior without changing its source code.

## What it does

* Limits the scan to **20 requests/second**.
* Runs the scan for **120 seconds**.
* Preserves Feroxbuster's **state** so recursive scans can resume without starting over.
* Pauses for **7 minutes** after each scan window.
* Automatically resumes the scan after the cooldown.
* Uses --scan-limit 1 to reduce concurrent recursive scans and make the request rate more predictable.

## Workflow

Sending 20 Requests Persecond => 120s scanning => 7min cooldown => resume => repeat


The goal is to reduce aggressive request bursts and make reconnaissance traffic more controlled.

## Setup/Usage
-1 go to a preferd Directory " cd /home/kali/Tools "

-2 Creat a file " nano ferox_low_noise.sh " and Put The Code on the bash File

-3 make the file excutble " chmod +x ~/ferox_low_noise.sh " 

-4 make sure the File bash File have the Right permissons " -rwxr-xr-x ... ferox_low_noise.sh "

-5 Rin the Bash File and Put the Target https://Target IP and the wordlist path /usr/share/seclists/Discovery/Web-Content/common.txt

-6 the Output File will be In this Path /home/kali/ferox_states

### How To use it 
* run The Bash Script in the terminal:  /home/kali/Tools/ferox_low_noise.sh  https://Target IP  /usr/share/seclists/Discovery/Web-Content/common.txt

___________________________________________________________________

# 👾Editing Simple Tools With Simple Code👾!

I'm trying to edit the tools that I use to work against targets that use security systems such as WAFs, IDS/IPS, and firewalls.

I've studied Blue Team tactics to discover how attackers are detected and how firewalls, WAFs, and IDS/IPS are configured to detect attackers through patterns such as a high volume of requests in a short period of time, sustained request volumes over a longer period, aggressive scans, etc.

My goal is to perform my reconnaissance process without the headache of triggering security systems.

I'm mainly focusing on web penetration testing now, so I'll only work on tools related to web penetration testing.
