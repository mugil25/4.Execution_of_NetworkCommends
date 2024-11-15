# 4.Execution_of_NetworkCommands
### NAME: MUGIL M.
### REG NO: 212223230127
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
## PROGRAM:
CLIENT:

```
**import socket 
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
SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## TRANCEROUTE COMMAND:
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## Output

PING COMMAND:

CLIENT:

![Screenshot 2024-11-06 184210](https://github.com/user-attachments/assets/d1cd2d88-42f6-46bb-b020-47d5abc2a62b)


SERVER:

![Screenshot 2024-11-06 184143](https://github.com/user-attachments/assets/d2be5386-4f29-475c-9c5a-bacb6fab77f0)

TRANCEROUTE COMMAND:

![Screenshot 2024-11-09 172007](https://github.com/user-attachments/assets/a5346502-23e1-4fa0-9503-d38f5b4dd0a9)

## Result
Thus Execution of Network commands Performed 
