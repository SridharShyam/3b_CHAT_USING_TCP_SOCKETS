# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM: 
Name: SHYAM S  
Register No: 212223240156 
### CLIENT: 
``` 
import socket

client = socket.socket()
client.connect(('localhost', 8000))

while True:
    message = input("Client > ")
    client.send(message.encode())

    reply = client.recv(1024).decode()
    print("Server >", reply)

```
 
### SERVER: 
``` 
import socket

server = socket.socket()
server.bind(('localhost', 8000))
server.listen(1)
print("Waiting for client...")

client, address = server.accept()
print("Connected to", address)

while True:
    message = client.recv(1024).decode()
    print("Client >", message)

    reply = input("Server > ")
    client.send(reply.encode())

```
## OUTPUT
![image](https://github.com/user-attachments/assets/00a4b7fb-274f-4ecd-a15b-c40548a85ee1)

![image](https://github.com/user-attachments/assets/22f5d2dd-9a57-4692-9382-ff0e0c76735c)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
