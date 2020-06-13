
## How to protect from port scanning and smurf attack in Linux Server by iptables

### June 15, 2013 by Sharad Chhetri 20 Comments

In this post I will share the iptable script in which we will learn How to protect from port scanning and smurf attack in Linux Server.

Features Of Script :

(1) When a attacker try to port scan your server, first because of iptable attacker will not get any information which port is open. Second the Attacking IP address will be blacklisted for 24 Hour (You can change it in script) . Third , after that attacker will not able to open access anything for eg. even attacker will not see any website running on server via web browser, not able to ssh,telnet also. Means completely restricted.

(2) Protects from smurf attack

(3) Written with the help of IPTABLE hence no System Performance issue like CPU high,Memory usage etc. No third party tool is used

Note: You can add or remove port no. as per your requirement.
Now we will create the script

Step 1: Create a bash script with the name of iptablescript.sh

vi /root/iptablescript.sh
Step 2: Now paste the below given script contents in your bash script file iptablescript.sh
Step 3: Make the Read Write Execute permission only to root user. (For security)
chmod 700 /root/iptablescript.sh
  chown root:root /root/iptablescript.sh
Step 4 : Now run the script
./root/iptablescript.sh
Step 6: Now check the IPTABLES rule with following command
iptables -nL
