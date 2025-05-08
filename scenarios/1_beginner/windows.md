🗂️ Scenario 2: Cracking Microsoft Office Passwords (Intermediate)
Objective:
Introduce Microsoft Office encryption formats, hash extraction, and targeted cracking with Hashcat.
Narrative Setup:
A team at a small company lost access to a critical .docx file. IT is asked to recover it for continuity.
Files & Tools Provided:
A password-protected .docx (you can create it manually)
Python script: office2hashcat.py (from hashcat-utils)
Steps to Extract the Hash:
bash
CopyEdit
python3 office2hashcat.py secret.docx > office_hash.txt
Hash Modes Overview:
Office Version
Hash Mode
≤ 2003
9700
2007
9400
2010
9500
2013
9600
2016+
9720
Cracking Example (for Office 2013):
bash
CopyEdit
hashcat -m 9600 office_hash.txt wordlist.txt --force
Teaching Points:
Emphasize how newer Office formats use strong key derivation (e.g., SHA-1, AES, PBKDF2).
Compare GPU vs. CPU performance — show why GPU acceleration is critical.
Explain the limits of brute force and the power of good wordlists and targeted guesses.
