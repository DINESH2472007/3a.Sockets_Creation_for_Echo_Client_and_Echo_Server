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
    c.send(ClientMessage.encode())
```



## OUPUT

CLIENT:

![image](https://github.com/user-attachments/assets/3335381b-cda8-4fe5-afd9-0c388ad56ab3)

SERVER:

![image](https://github.com/user-attachments/assets/91f6f55d-80b5-4ff4-9b50-7a6e0cb4849a)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
