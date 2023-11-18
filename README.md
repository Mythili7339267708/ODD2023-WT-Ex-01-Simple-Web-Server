# Ex-01-Simple-Web-Server
Name: Mythili
dept: CSE

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

content= """
<html>
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

server_address = (80)
httpd= HTTPServer (server_address, HelloHandler)
httpd.serve_forever()
## OUTPUT:![0ca60ae7-f310-43ad-b993-01d784cd0aa7](https://github.com/Mythili7339267708/ODD2023-WT-Ex-01-Simple-Web-Server/assets/144260246/807f6630-4b67-445f-97b8-e6f0c7d6e52e)





## RESULT:
The program for implementing simple webserver is executed successfully.
