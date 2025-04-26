You are an elite member of the hacking collective AntiBigBank -- a group dedicated to exposing corporate negligence.
Your current target is **Big Bank,** a major financial institution that allegedly failed to protect its customer data.

Through deep recon, your team discovered that Big Bank's internal Linux server - the vault where they store sensitive user accounts - is vulnerable.

This is your opportunity to exploit their carelessness.


Intelligence Report:
One of our operatives successfully planted a Wi-Fi Pineapple device inside Big Bank's network. During the operation, they intercepted an HTML file contained internal server information. However, some of the file's content were corrupted, scrambling the data.

The page contains fragments of sensitive data, including what appear to be password hashes. Only one hash can grant you deeper access to the server via SSH.

Your team has deployed a Kali Linux machine deep inside their internal network for this operation.
	Warning: Big Bank's firewall will not detect traffic from tools like Hashcat, John the Ripper, or Hydra -- but stay disciplined and only use these authorized methods to avoid detection.


Your Challenge (Should you choose to accept it):
1. Scrub through the website's corrupted contents carefully.
2. Identify the correct password hash for Big Bank's SSH terminal access.
3. Crack the hash to recover the login password
4. Gain remote access to Big Bank's internal server
5. Escalate privileges once inside.
6. Locate and steal the master password hashes stored in /etc/shadow.
7. Crack the stolen hashes to fully compromise user accounts.


The more accounts you recover, the stronger the message we send: AntiBigBank does not play games.



Rules of Engagement:
You may only use tools and techniques authorized by Big Bank protocols (Kali Linux tools, Hashcat, standard enumeration techniques).

No unauthorized network disruption (stay within your lab environment).

Collaboration between team members is encourages.


Victory Conditions:
Successful SSH login with the cracked credential.
Root-level access obtained through privilege escalation.
At least one user password cracked form the stolen /etc/shadow file.

**Operation AntiBigBank - Mission Checklist**
🛠 Phase 1: Reconnaissance
 Access the compromised internal webpage (hosted on Big Bank's server).

 Scrub through the messy HTML data carefully.

 Identify the correct password hash intended for SSH access.

🔓 Phase 2: Password Cracking
 Extract the identified hash.

 Crack the password hash using approved tools (Hashcat, John the Ripper, or Hydra).

 Recover the SSH login password.

🖥 Phase 3: Gaining Access
 SSH into the Big Bank Linux server using the cracked credentials.

 Confirm successful login.

📈 Phase 4: Privilege Escalation
 Enumerate the system for privilege escalation vectors (SUID files, sudo misconfigurations, etc.).

 Gain root-level access.

🗄 Phase 5: Data Exfiltration
 Locate and extract the /etc/shadow file containing user password hashes.

 Exfiltrate the file to your attacker machine safely.

🔥 Phase 6: Dominate
 Crack as many user passwords as possible from the stolen /etc/shadow.

 Document recovered user credentials.

🏆 Victory Conditions
 SSH access obtained using cracked credentials.

 Root-level access achieved through escalation.

 At least one user password cracked from /etc/shadow.

🎯 Pro Tips:
Work methodically: rushing leads to mistakes.

Share findings with teammates — collaboration is key.

Keep notes of cracked passwords and escalation paths.


Remember:
Every account compromised weakens Big Bank’s defenses and strengthens AntiBigBank’s message to the world.

Good luck,
Big Bank's time is up.
vididco(Fgq F)
