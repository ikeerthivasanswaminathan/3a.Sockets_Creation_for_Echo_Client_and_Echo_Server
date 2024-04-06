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

![ex3aclient](https://github.com/ikeerthivasanswaminathan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148937372/7ffef7b1-b51d-4aad-8834-872b34a5f4ce)

Server

![ex3aserver](https://github.com/ikeerthivasanswaminathan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148937372/91efce7c-8eb7-4824-9b2e-11333d44ec64)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets links was successfully created and executed.
