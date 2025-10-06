# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# NAME:R.TEJASWINI
# REG NO:212224230218
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
5. 
## PROGRAM
# server:

import socket

s=socket.socket()

s.bind(('localhost',8001))

s.listen(5)

c,addr=s.accept()

while True:

    ClientMessage=c.recv(1024).decode()
    
    c.send(ClientMessage.encode())
    
# client:

import socket

s=socket.socket()

s.connect(('localhost',8001))

while True:

    msg=input("Client > ")
    
    s.send(msg.encode())
    
    print("Server > ",s.recv(1024).decode())

            
## OUTPUT:

<img width="1744" height="186" alt="Screenshot 2025-10-06 110601" src="https://github.com/user-attachments/assets/edafa9bc-1d47-444b-8242-4eb28555010d" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
