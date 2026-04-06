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

