# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
## CLIENT
![5](https://github.com/Rajkiran276/3b_CHAT_USING_TCP_SOCKETS/assets/147471453/c62fb851-2c18-4dc1-bb86-55215f62b6fa)

## SERVER
![6](https://github.com/Rajkiran276/3b_CHAT_USING_TCP_SOCKETS/assets/147471453/43abc446-75ea-4b3e-8809-96d1e912bfbd)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
