# Developing a Simple Webserver
Name: ajay
ID: 23007325

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<body>
<h1>Welcome</h1>
</body>
</head>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:

```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<body>
<h1>Welcome</h1>
</body>
</head>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```

# OUTPUT:
![output]
![webserver1](https://github.com/Ajayreddy-2006/Web_server/assets/145742508/c000ae31-9507-4297-bb9c-8f8db16d2831)

# RESULT:




















































































































































The program is executed succesfully
