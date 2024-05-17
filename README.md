# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Server Side
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
### Client Side
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUPUT
### server:
![Screenshot 2024-05-14 142510](https://github.com/lokeshrahulv/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118423842/24292fb6-d089-4476-9a7c-94d533497dd1)
### client
![Screenshot 2024-05-14 142521](https://github.com/lokeshrahulv/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118423842/d37aabc6-803c-44c1-b9f2-0f83cbe4535b)
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
