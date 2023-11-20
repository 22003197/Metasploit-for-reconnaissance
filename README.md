# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
Find out the ip address of the attackers system
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/5796d7d8-db18-4462-ba61-1f3e2f066d9a)
## invoke msfconsole:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/f532092d-5f20-4268-96a4-d85e939ce4ad)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

## OUTPUT:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/404b30ea-57ef-4914-a9ba-fea347e383b1)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/b06c3517-6e5e-4406-b592-157ad0967023)
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
## Output:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/3e26356a-5793-416f-94ab-191f3e320183)
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/132e875d-8bb0-4f9f-b15f-3f1c4cd8e69b)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/494366b2-8772-4904-93eb-7673431ca05e)
The info command provides information regarding a module or platform.
## Output:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/5d9b5980-852d-49d8-95ed-ad39fe6e3810)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>.
## Ouput:
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/b68d6d95-2023-41cd-a80c-96fc5e2fcf31)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/315f9158-6b98-4a7e-b891-c37d23f8c8aa)
Use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/627c7c4c-a095-49c3-86a0-155baef0bd75)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/211f4957-3ac0-455e-87a6-695257dbae2b)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/bbde02c9-a257-45d2-aebd-e969bd2c2fcf)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.
![image](https://github.com/22003197/Metasploit-for-reconnaissance/assets/124332243/c3699c37-a78c-4811-ac80-380428657e2f)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
