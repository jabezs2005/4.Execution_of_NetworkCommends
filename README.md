# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Algorithm:
<BR>
Step 1: start the program.
<BR>
Step 2: Include necessary package in java.
<BR>
Step 3: To create a process object p to implement the ping command.
<BR>
Step 4: declare one Buffered Reader stream class object.
<BR>
Step 5: Get the details of the server
<BR>
 5:1: length of the IP address.
 <BR>
 5:2: time required to get the details.
 <BR>
 5:3: send packets, receive packets and lost packets.
 <BR>
 5.4: minimum, maximum and average times.
 <BR>
Step 6: print the results.
<BR>
Step 7: Stop the program.
<BR>

## Program:
**CLIENT:**
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost'8000))
s.listen(5)
c,addr=s.accept()
while True:
 hostname=c.recv(1024).decode()
 try:
 c.send(str(ping(hostname, verbose=False)).encode())
 except KeyError:
 c.send("Not Found".encode())
```
**SERVER:**
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 ip=input("Enter the website you want to ping ")
 s.send(ip.encode())
 print(s.recv(1024).decode())
```
### Output:
## CLIENT:
![Screenshot 2024-04-05 132526](https://github.com/jabezs2005/4.Execution_of_NetworkCommends/assets/147473463/9ebfeb17-d719-4989-a87d-af3a175c2829)
## SERVER:
![Screenshot 2024-04-05 132557](https://github.com/jabezs2005/4.Execution_of_NetworkCommends/assets/147473463/747e03a3-ad2d-4a87-b872-5405ddc456dc)

## Result
Thus Execution of Network commands Performed.
