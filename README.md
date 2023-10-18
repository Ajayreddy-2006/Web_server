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
<<<<<<< HEAD
![output](webserver-1.jpg)
=======
![Alt Text](https://github.com/Ajayreddy-2006/Web_server/blob/89db7fb1ade387d879ad62c742e888ae1e521f0a/images/Screenshot%202023-10-05%20093908.png)
>>>>>>> f0233cadc7f47f6c278bdc3c912fe59694982f31

# RESULT:


<<<<<<< HEAD


















































































































































The program is executed succesfully
=======
The programe is executed succesfully
>>>>>>> f0233cadc7f47f6c278bdc3c912fe59694982f31
