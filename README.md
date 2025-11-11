# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
#### CLIENT:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
#### SERVER:
```python
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

## OUPUT
#### CLIENT:
<img width="497" height="182" alt="Screenshot 2025-11-04 223001" src="https://github.com/user-attachments/assets/385ff360-03a5-42ab-bddf-9188974e5a51" />

#### SERVER:
<img width="510" height="213" alt="Screenshot 2025-11-04 222956" src="https://github.com/user-attachments/assets/3b147305-cf9a-41ca-9763-97781abb9398" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
