# EX NO: 1- Echoserver
Echo server and client using python socket

# AIM:
To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:
### Step 1:
Design of echo server and client using python socket
### Step 2:
Implementation using Python code
### Step 3:
Testing the server and client 

## PROGRAM:
# Client
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'PRASANNA A, 212223220078')
    print(f'Received: {s.recv(1024)!r}')
```
# Serevr
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/f2651b78-3cb8-4c50-9cd8-14f2d1724a28)

## RESULT:
The program is executed successfully
