# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### Name: Anu Varshini M B
### Register Number: 212223240010
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```
### Server:
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
## OUPUT:
### Client:
![Screenshot from 2024-10-16 11-03-22](https://github.com/user-attachments/assets/ae817870-7046-4144-b1a9-e2ab82513a97)


### Server:
![Screenshot from 2024-10-16 11-03-29](https://github.com/user-attachments/assets/6fb0fc8b-564c-47d7-a776-0d0ffe9913d1)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
