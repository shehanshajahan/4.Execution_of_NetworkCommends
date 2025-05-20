# 4.a.Execution_of_Network_Commands
## Name : Shehan Shajahan
## Registration Number : 212223240154
## AIM :
To write the python program for simulating ping command and to write the python program for simulating Traceroute command.
## Software : 
Command Prompt And Network Protocol Analyzer
## Algorithm For PING :
```
Step 1: start the program.
Step 2: Include necessary package in java.
Step 3: To create a process object p to implement the ping command.
Step 4: declare one Buffered Reader stream class object.
Step 5: Get the details of the server
5:1: length of the IP address.
5:2: time required to get the details.
5:3: send packets, receive packets and lost packets.
5.4: minimum, maximum and average times.
Step 6: print the results.
Step 7: Stop the program.
```
## Algorithm For TRACEROUTE :
```
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will send NACK signal to client.
6. Stop the program
```
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

## PING
## PROGRAM :
## Client :
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
## Server :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   ip=input("Enter the website you want to ping ")
   s.send(ip.encode())
   print(s.recv(1024).decode())
```

## Output: 
![Screenshot 2025-04-16 105319](https://github.com/user-attachments/assets/34fd5dbc-f52f-4605-bc87-eb50b7163eed)

## TRACEROUTE
## Command :
```
tracert www.facebook.com
```
## Output :
![image](https://github.com/user-attachments/assets/26bc98d0-9a26-4f4f-b433-ce755634d1ee)

## Result
Thus Execution of Network commands Performed.
