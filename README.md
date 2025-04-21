# EX01 Developing a Simple Webserver
## Date: 21.04.2025

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
  <!DOCTYPE html>
  <head>
      <title>LAPTOP CONFIGURATION</title>
  </head>
  
  <body><center>
      <h1>My laptop configuration</h1>HARISH G<h1></h1></center>
      <table border="100px" align="center" cellpadding="10" style="background-color: rgb(76, 76, 205);" >
      <tr style="color: black; ">
          <th>DEVICE SPECIFICATION</th>
          <th>DETAILS</th>
      </tr>
      <tr style="color: rgb(0, 0, 0); ">
          <td>BRAND</td>
          <td>LENOVO</td>
      </tr>
      <tr>
          <td>MODEL NAME</td>
          <td>E16 GEN 4</td>
      </tr>
      <tr>
          <td>SCREEN SIZE</td>
          <td>15.6 inches</td>
      </tr>
      <tr>
          <td>COLOR</td>
          <td>BLACK</td>
      </tr>
      <tr>
          <td>RAM</td>
          <td>16GB</td>
      </tr>
      <tr>
          <td>ROM</td>
          <td>512GB</td>
      </tr>    
      <tr>
          <td>HARD DISK</td>
          <td>CORE i5</td>
      </tr>
      <tr>
          <td>GRAPHICS CARD</td>
          <td>NVIDIA</td>
      </tr>
      <tr>
          <td>SYSTEM TYPE</td>
          <td>64 BIT-OS,X64</td>
      </tr>
  </table>
  
  </body>
```

## Simplewebserver:
```
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```


## OUTPUT:
![WhatsApp Image 2025-04-21 at 9 28 45 PM](https://github.com/user-attachments/assets/42532ed1-51af-402c-a768-9265c0a5c605)
![Screenshot 2025-04-21 212733](https://github.com/user-attachments/assets/04641ffa-3790-470e-a5e3-ae9545085e52)


## RESULT:
The program for implementing simple webserver is executed successfully.
