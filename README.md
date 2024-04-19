# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server.
4. Send and receive the message using the send function in socket.

## PROGRAM

client.py

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```

server.py

```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode()) 
```

## OUPUT

Client

![ex3aclient (edited)](https://github.com/ikeerthivasanswaminathan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148937372/a80f5fbd-0887-431f-8e30-c345faa43127)

Server

![ex3aserver (edited)](https://github.com/ikeerthivasanswaminathan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148937372/99e80f05-7ccc-4134-b963-b5c18fe738a4)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets links was successfully created and executed.
