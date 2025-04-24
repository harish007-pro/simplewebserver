# EX01 Developing a Simple Webserver
## Date: 24.04.2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
    <head>
        <title>
            TCP/IP
        </title>
    </head>
    <body bgcolor="white">
       <center> <font color="Blue" size="100" >TCP/IP PROTOCALS<br></font></center>
        <h2>1.Application Layer HTTP, FTP, SSH, TELNET & DNS. </h2>

        <h2> 2.Transport Layer TCP, UDP.</h2>
            
        <h2>3.Internet Layer ICMP, IGMP, ARP, IPv4/IPv6. </h2>

        <h2>4.Network Access Layer Ethernet, FDDI, X.25, Frame Relay , Token Ring. </h2>
        
    
    </body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```


## OUTPUT:
![Screenshot 2025-04-21 172426](https://github.com/user-attachments/assets/0cda3408-ffc9-4bbb-9601-d5cd1452435c)



## RESULT:
The program for implementing simple webserver is executed successfully.
