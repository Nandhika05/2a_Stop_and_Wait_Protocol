# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

Name : Nandhika P

Register Number : 212223040125

## Client:
```
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
```
## Server:
```
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT
Client :-

![Screenshot 2024-10-06 165102](https://github.com/user-attachments/assets/c747963a-29c8-416b-ab1a-d9935b3376e0)

Server:-

![Screenshot 2024-10-06 165125](https://github.com/user-attachments/assets/e1c62f5f-435d-4b6f-b203-835417f1cfae)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
