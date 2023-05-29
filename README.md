# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE :26-04-2023
## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :
1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server.

4.Send and receive the message using the send function in socket.

# PROGRAM :
# CLIENT :
### Developed by:D. Vinitha Naidu
### Register No: 212222230175
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
# SERVER :
### Developed by:D.Vinitha 
### Register No: 212222230175
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
## OUTPUT :
## CLIENT :
![image](https://github.com/VinithaNaidu/EX-8/assets/121166004/6b2bbbeb-0ece-4dc9-9e7a-b6979a925c1d)

## SERVER :
![image](https://github.com/VinithaNaidu/EX-8/assets/121166004/a6620927-ea4e-4d38-b9ad-cd934c623f39)


## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

