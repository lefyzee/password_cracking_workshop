# How to use Hashcat on Kali Linux

This guide is a beaginner-friendly intro to using Hashcat. It is a powerful password cracking tool that should already be installed on the VM and the Kali USB.

Lets get started!
Test on a hash you made
- Make sure you are booted into the Kali USB Stick or VM
- Launch a terminal window

- run 'openssl passwd -6 password123'
- Copy that output to a file using 'openssl passwd -6 password123 > test_hash.txt'
- Then you can check the hash using 'cat test_hash.txt'

- Now you are ready to use Hashcat!
- now to crack the hash we will run it through rockyou.txt using command 'hashcat -m 1800 -a 0 test_hash.txt /usr/share/wordlists/rockyou.txt --force'
-   -m 1800 specifies the hash type. In our case Linux SHA-512 like the one found in /etc/shadow
-   -a 0 is a straight attack using a wordlist
-   You need to use the --force command if you are running kali on a virtual machine

- After the command has run use the command 'hashcat -m 1800 -a 0 test_hash.txt /usr/share/wordlists/rockyou.txt --show' to see the hash

- You have cracked the SHA-512 Hash! Congrats! Have fun cracking passwords.
