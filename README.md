3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
AIM
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

ALGORITHM:
Import the necessary modules in python
Create a socket connection to using the socket module.
Send message to the client and receive the message from the client using the Socket module in server .
Send and receive the message using the send function in socket.
PROGRAM
server:
import socket
'''
HOST = '127.0.0.1'  
PORT = 65432        

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as server_socket:
    server_socket.bind((HOST, PORT))
    server_socket.listen()

    print(f"Server is listening on {HOST}:{PORT}")
    while True:
        conn, addr = server_socket.accept()
        with conn:
            print(f"Connected by {addr}")
            while True:
                data = conn.recv(1024)
                if not data:
                    break
                conn.sendall(data)
                print(f"Echoed: {data.decode('utf-8')}")'''
client:
'''
import socket

HOST = '127.0.0.1'  
PORT = 65432  

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as client_socket:
    client_socket.connect((HOST, PORT))

    message = 'Hello, Server!'
    client_socket.sendall(message.encode('utf-8'))

    data = client_socket.recv(1024)
    print(f"Received echo: {data.decode('utf-8')}")'''
OUPUT
![373115439-ff611de3-ecb3-42b3-9b2c-c7ce151018e6](https://github.com/user-attachments/assets/189b56c9-2e1a-4ef5-94f4-665625c11e74)

![373115472-7c54f430-d3be-45bb-b4d7-bebcec3a54ff](https://github.com/user-attachments/assets/279802cb-5218-4570-954e-24d4103aa933)

RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
