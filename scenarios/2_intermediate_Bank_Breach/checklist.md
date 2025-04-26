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