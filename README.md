# eJPT-cheat-sheet
Command study guide for the eJPT exam.

The eLearn Junior Penetration Tester exam is a great exam if you're looking for an entry level certification in penetration testing. INE's training covers everything you need to know for the exam. I would reccomend some additional resources for pivoting across networks. 


### NMAP
```
$namp -p 1-65535 <IP ADDRESS>.0/24
$nmap -p --script=vuln -v 
$nmap -sV --script=vulners -v <IP ADDRESS>

https://www.tutorialspoint.com/nmap-cheat-sheet
```
### IP Route
```
$route
$ip route add <Address Range> via <Router IP> <Interface>

https://www.cyberciti.biz/faq/ip-route-add-network-command-for-linux-explained/
```
#### Pivoting Help
```
https://pentest.blog/explore-hidden-networks-with-double-pivoting/
```
### NCRACK
```
$ncrack -U /userlist.txt -P /passwordlist.txt ftp://IPADDRESS

https://www.kalilinux.in/2021/02/ncrack.html
```
### Hydra
```
$hydra -v -V -u -L usersList.txt -P passwordslist.txt -u <IP ADDRESS> SSH
(Switch SSH for FTP if needed)

https://www.freecodecamp.org/news/how-to-use-hydra-pentesting-tutorial/
```

### John The Ripper
```
$unshadow /etc/passwd /etc/shadow > output.txt
$john output.txt

https://www.freecodecamp.org/news/crack-passwords-using-john-the-ripper-pentesting-tutorial/
```
### Dirb
```
$dirb http://URLhere

https://www.hackingarticles.in/comprehensive-guide-on-dirb-tool/
```
### SQLMap
```
$sqlmap -u "http://URLhere/login.php"
$sqlmap -u 'http://URLhere/file.php?id=1" -p id

https://github.com/sqlmapproject/sqlmap/wiki/Usage
```
### SMB
```
$smbmap -H <IP ADDRESS>
$nmblookup -A <IP ADDRESS>
$enum4linux -a <IP ADDRESS>
$smbclient //IPADRESS/SHARENAME

https://fareedfauzi.gitbook.io/oscp-notes/services-enumeration/smb
```
### Meterpreter
```
If you are working in a virtual machine be sure to set LHOST to tap0 rather than the interface IP address. 

https://www.offsec.com/metasploit-unleashed/meterpreter-basics/
```
### Windows Commands
```
dir
list disk
type <textFileName>.txt
net accounts
net users

https://book.hacktricks.xyz/windows-hardening/basic-cmd-for-pentesters
```

