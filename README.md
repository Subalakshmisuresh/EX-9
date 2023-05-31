# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

DATE :

AIM:

To write a python program for creating Chat using TCP Sockets Links.

ALGORITHM:

1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program

PROGRAM:

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
SERVER:
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
OUTPUT:


CLIENT:

![image](https://github.com/Subalakshmisuresh/EX-9/assets/121957896/a775992b-b9ec-4239-a316-0efba38e3626)

SERVER:

![image](https://github.com/Subalakshmisuresh/EX-9/assets/121957896/b6eece2f-8eda-40a5-a2b0-02bf6472f1e6)

RESULT:

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.



