# Ex-01-Simple-Web-Server
NAME:Salini.A
DEPT:IT
REF:23008741
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('',80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()


## OUTPUT:




![webserver](https://github.com/salinianbzhgan/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742862/3f1819c9-a2ff-47b9-b905-e9e92d403417)

## RESULT:
The program for implementing simple webserver is executed successfully.
