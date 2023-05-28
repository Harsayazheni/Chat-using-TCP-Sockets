# Chat-using-TCP-Sockets
CREATION FOR CHAT USING TCP SOCKETS
EXP: 6
DATE:
AIM:
To write a python program for creating Chat using TCP Sockets Links.
ALGORITHM:
1.
2.
3.
4.
5.
Start the program.
Get the frame size from the user.
To create the frame based on the user request.
To send frames to server from the client side.
If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program
PROGRAM:
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
SERVER:
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
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())
OUTPUT:
CLIENT:
![Screenshot from 2023-05-28 21-27-02](https://github.com/Harsayazheni/Chat-using-TCP-Sockets/assets/118708467/4cd4ddb5-9255-42b3-86dc-290edc2d1150)
SERVER:
![Screenshot from 2023-05-28 21-27-08](https://github.com/Harsayazheni/Chat-using-TCP-Sockets/assets/118708467/816b0e5b-bfa9-4d6e-a0fe-86afb4776120)

