# Notes:
📋 Step-by-Step Planning Guide
Action Items:
40 People max
-Room reserved
-Flyer being made
Keep organized in GitHub
Marketing

1. Collaborative Planning (Your Meeting Agenda)
Introduce the idea: Explain the workshop’s purpose and how both clubs benefit.


Discuss logistics:
Date & time: May 15 2025
Location or platform (in-person and virtual?)
Number of participants 40
Equipment needed (laptops VMs)

Assign roles:
Brandon: plan scenarios
Ata: Create Presenation
Ian: Help plan scenarios and technical structure


Who will teach?
Ata

Who’s handling setup?
Brandon

Who’s doing outreach/promotion?
Everyone

2. Workshop Structure
Here’s a suggested flow:
🧠 Part 1: Quick Theory (20–30 mins)
What is password cracking?

Why do hackers crack passwords?

Common types of hashes (MD5, SHA-1, bcrypt)

Password policies and why they matter


💻 Part 2: Demo & Hands-On (45–60 mins)
Show how hashing works

Use tools like:
hashcat or John the Ripper

rockyou.txt wordlist

Optional: Crack a ZIP file, Word document, or local Linux user password hash

Walk students through cracking a few test passwords in a safe environment (like a prepared VM or lab machine)


🎯 Part 3: Challenge (Optional, Fun)
Teams or individuals race to crack a set of hashes


Reward the winners (stickers, swag, shout-out)


🔐 Part 4: Defense Tips (10 mins)
Strong password creation strategies
Password managers
Multi-factor authentication (MFA)



🧰 Tools & Resources
Kali Linux or any Linux VM
John the Ripper, Hashcat, hydra (for web/brute-force examples)
rockyou.txt wordlist (built into Kali)
Pre-prepared sample hashes (from test passwords)
Slides or visual aids



🛡️ Ethics & Legal Safety
Only crack legally obtained, pre-approved, or test passwords
Include a disclaimer: this is for education only
Remind everyone to never attempt this on real systems or accounts
You might even have an agreement/waiver form depending on your college’s policy



🗣️ Pro Tips for the Meeting
Emphasize student learning and career relevance (e.g., CEH, CPTC prep)
Offer to share responsibilities equally
Be open to feedback from the other club—they might bring fresh ideas


# Attacks:
🧠 1. Brute Force Attack
How it works:
 Tries every possible combination until it finds the correct one.
 Pros: Guaranteed success (eventually)
 Cons: Extremely slow for long or complex passwords
Tool example: John the Ripper, Hydra

📚 2. Dictionary Attack
How it works:
 Uses a precompiled list of common passwords (e.g., rockyou.txt) to try matches.
 Pros: Faster than brute force
 Cons: Fails if password is unique or complex
Tool example: John, Hashcat, Hydra

🧠💡 3. Hybrid Attack
How it works:
 Combines a dictionary with common patterns (e.g., adding 123 or capitalizing the first letter).
 Pros: Good for cracking human-style passwords
 Cons: Still limited to predictable patterns
Tool example: Hashcat rules (best64.rule, d3ad0ne.rule)

🧮 4. Rainbow Table Attack
How it works:
 Uses precomputed hashes for possible passwords and compares them to the target hash.
 Pros: Fast if the table contains the hash
 Cons: Useless against salted hashes
Tool example: rtgen, rcracki_mt

🔍 5. Credential Stuffing
How it works:
 Takes username/password combos from leaks and tries them on other sites.
 Pros: Very effective due to password reuse
 Cons: Requires leaked credentials
Tool example: Sentry MBA, Snipr, or Python scripts

🌐 6. Phishing (Social Engineering)
How it works:
 Tricks the user into giving up their password via fake login pages or emails.
 Pros: Doesn’t require computing power
 Cons: Risky, often illegal without consent
Note: Can be mentioned for awareness but not demoed in your workshop unless it’s fully simulated and ethical.

🧱 7. Keylogging
How it works:
 Records keystrokes to steal passwords as they’re typed.
 Pros: Captures passwords directly
 Cons: Needs to be installed on target system
Again: Only talk about this as a threat, not something to do.

🛠️ 8. Exploiting Poorly Secured Systems
How it works:
 Some systems store passwords in plaintext or weak hashes, making them easy to crack.
 Example: Extracting /etc/shadow hashes from a Linux VM and cracking them offline

⚠️ Bonus: Offline vs Online Cracking
Offline: Cracking a dumped hash file (e.g., from /etc/shadow) – faster, safer to demo


Online: Trying passwords directly on a login page – riskier, slower, easier to detect





# Scenarios:
🕵️‍♂️ Workshop Scenario: Operation Breach Simulation (Beginner)
🎬 Scenario Premise
You and your team are ethical hackers working with a cybersecurity firm. You’ve been hired to investigate a recent fictional data breach of a shady online bank suspected of money laundering. Your mission is to:
Analyze the leaked password hashes


Crack them using open-source tools


Gain access to dummy “bank accounts”


Identify how much fake money was exposed


Write a report on how the breach happened and recommend defenses



🛠️ What Participants Will Do
Use tools like John the Ripper or Hashcat to crack sample hashes


Access a mock banking web app (local or simulated environment)


Use credentials to “log in” to accounts


Discover fun Easter eggs or fake balances


Report what they found (for points)



🎯 Learning Objectives
By the end of this mission, participants will:
Understand how password hashes are cracked


Learn about weak vs. strong password policies


See how real-world breaches can escalate


Practice ethical hacking under controlled conditions



🧪 Optional Fun Additions
Leaderboards: Who cracked the most passwords?


Hidden Flags: Like a mini CTF (Capture the Flag)


Report Template: Each team writes a 5-minute debrief with:


How many passwords they cracked


How the breach could’ve been prevented



🛡️ Ethical Note
At the start of the workshop, clearly state:
"Everything in this simulation is fictional. This is a safe environment to learn how hackers operate so you can defend against them in the real world. Never attempt these techniques on real systems without permission."
🗂️ Scenario 2: The Leaked Employee Laptop (Beginner)
🎬 Scenario Premise
A government employee at the fictional Department of Urban Safety lost their encrypted laptop at a coffee shop. You’ve recovered the hard drive and need to investigate whether any sensitive data was at risk.
Your job:
Access the user’s local files


Extract and crack the hashed system password


Explore local documents to identify security risks


Report your findings



🛠️ What Participants Will Do
Mount a Linux VM image or ZIP folder representing the "laptop"


Use unshadow + John the Ripper to crack the user password


Explore the file system for clues (e.g., passwords in .txt files, weak encryption, password reuse)


Submit a summary of what they found



🎯 Learning Objectives
Practice offline password cracking from Linux systems


Understand the risks of storing sensitive data insecurely


Learn basic forensics techniques



Bonus Features
Add decoy files like passwords.txt, SSN_backup.docx


Hide hints inside files (Easter eggs)



🧑‍💼 Scenario 3: Insider Threat at MegaCorp (Intermediate)
🎬 Scenario Premise
You’re part of MegaCorp's internal security team. HR suspects an insider is planning to exfiltrate customer data. IT gave you access to the suspect’s workstation image. Your mission:
Crack their email and web app passwords


Access their inbox and cloud notes


Look for signs of leaked credentials or messages


Identify if a data breach was about to happen



🛠️ What Participants Will Do
Crack user passwords stored in browser files or exported hashes


Use fake credentials to log into a mock "MegaCorp Web Portal"


Explore browser history, saved logins, or fake emails


Identify any “leaked” internal files or notes



🎯 Learning Objectives
Learn about stored credential files and saved passwords


Understand insider threat vectors


Practice cracking browser passwords or web app credentials



Bonus Ideas
Use a fake email inbox (local HTML mockup)


Include suspicious messages like:


 “Meeting tonight. I uploaded the client list to tempstorage.net”




🔐 Final Tip for All Scenarios
Wrap each activity with a debrief:
What could the org have done better?


What would you recommend as a defender?


How does cracking play into a larger security posture?

🎯 Scenario 4: Operation Firewall Phantom (advanced)
🎬 Scenario Premise
The Global Cyber Defense Unit (GCDU) has intercepted a rogue operative named Agent Kestrel, a former insider turned digital mercenary. After a high-risk black site extraction by elite field agents Echo and Strix, a highly encrypted hard drive was recovered from a compromised data vault in the Alps.
Your mission:
Crack into the stolen hard drive


Investigate its contents for signs of espionage


Identify what secrets were at risk—and who was behind it


🕵️‍♂️ Time is limited. The data self-destruct mechanism is simulated to "wipe" after 90 minutes. Can you beat the clock?

🛠️ What Participants Will Do
Load a forensic image of the encrypted drive (simulated in a local VM or USB boot)


Identify and extract password hashes (e.g., /etc/shadow, browser data, KeePass database, etc.)


Deal with salted SHA-512 password hashes


Search for fragmented clues in files, metadata, or filenames


Piece together passwords or passphrases from subtle patterns



🧩 Suggested Technical Challenges
Strong salted hashes (SHA-512 or bcrypt with salt)


Multi-step clue chaining (e.g., find a note that reveals part of a password format or pattern)


Hidden password hints in EXIF metadata, shell history, or encrypted note fragments


Decoy accounts, files, and fake keys to mislead or delay



🎯 Learning Objectives
Understand how salted hashes protect against rainbow tables


Practice advanced password cracking strategies


Analyze the importance of secure password storage and endpoint security


Explore digital forensics and lateral thinking in a high-pressure simulation



🧪 Bonus Flavor
Fake “mission timer” countdown in the shell or dashboard UI


Folder names like Project_Aurora_Archive or Operative_Logbook_Encrypted


Files with red herrings like TOP_SECRET_DO_NOT_OPEN.docx


A corrupted KeePass database file with a challenging master password to brute-force



🛡️ Ethical Note
At the start of the workshop, remind participants:
"This entire scenario is fictional. All characters and events are purely educational. These skills are taught to strengthen security awareness and prepare defenders—not for unauthorized hacking."




