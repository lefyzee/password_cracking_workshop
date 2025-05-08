🔐 Scenario 1: Password Recovery from SHA-256 Hash (Beginner)
Objective:
Teach participants to crack simple SHA-256 password hashes using Hashcat with a wordlist and a custom rule.
Narrative Setup:
A graduate student encrypted their thesis with a password derived from a favorite book title + their birth year. They've forgotten the password but remember the general pattern.
Technical Setup:
Hash Mode: 1400 (SHA-256)
Hash File: thesis_hash.txt
Wordlist: books.txt
Example entries: gatsby, mockingbird, ulysses
Rule File (year_append.rule):
txt
CopyEdit
$1$9$9$0
$1$9$9$1
...
$1$2$0$2$5  (up to 2025)
Command Example:
bash
CopyEdit
hashcat -m 1400 thesis_hash.txt books.txt -r rules/year_append.rule --force
Teaching Points:
Demonstrates how password complexity is often overestimated.
Introduce the concept of rainbow tables vs. salting.
Suggest better practices: password managers, unique & complex passwords.
