## HTTP
**HTTP Hyper Text Transfer Protocol** is what is used whenever you view a website. It is the set of rules used for communicating with web servers for the transmitting of webpage data, whtether that is HTML, Images, Videos, etc.
**HTTPS Hyper Text Transfer Protocol Secure** is the secure version of HTTP. This data is encrypted and verifies the web server you are speaking to.

## Requests and Responses
- To access a website, your browser will need to make requests to a web server for assets such as HTL, Images and download the responses. For that, you need to tell the browswer where to access these resources, with URLs **Uniform Resource Locator**
- It´s mostly composed of these portions, with some being optional:
  - Scheme - The protocol used, such as HTTP, HTTPS or FTP.
  - Host - The domain name or IP addres of the server
  - Port - THe port you are going to connect to, usually 80 for HTTP and 443 for HTTPS
  - Path - The file name or location of the resource you are trying to access
  - Query String - Extra bits of information that can be sent to the request path.
  - Fragment - A reference to a location on the actual page request.

## Making a Request:
- You could use the Method GET / HTTP/1.1 to request data from an website.
- More data is sent via headers, which contain extra information to the web server.

GET / HTTP/1.1

Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
--HTTP Requests finish with a blank space, to signify it ended--

- Response:

HTTP/1.1 200 OK

Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98


<html>
<head>
    <title>TryHackMe</title>
</head>
<body>
    Welcome To TryHackMe.com
</body>
</html>

## HTTP Methods
- A way for clients to show their intended action when making an HTTP request. The main ones are:
  - GET
  - POST
  - PUT
  - DELETE

## HTTP Status Codes
- The first line of a response includes the protocol, the version, aswell as a status code.
- Some of the code ranges are:
  - 100-199 - Information Response - Sent to the client that the first part of their request has been accepted and they should continue sneding the rest of their requests.
  - 200-299 - Success - Request was successful
  - 300-399 -  Redirection - These are used to redirect the clients request to another resource, either to a different webpage or website.
  - 400-499 - Client Errors - Used to inform of an error with the request
  - 500-599 - Server Errors - ERrors that happened on the server-side and usually indicate quite a maor problem with the server handling the request.
 
## Common Codes 
- 200 - OK
- 201 - Created
- 301 - Moved Permanently - This redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead.
- 302 - Found - Similar to the above permanent redirect, but as the name suggests, this is only a temporary change and it may change again in the near future.
- 400 - Bad Request - Something was wrong or missing in the request, or a parameter was missing from the request.
- 401 - Not Authorised - Not allowed to view this resource since you are lacking authorisation with a username and password
- 403 - Forbidden - You do not have permission to see this content
- 405 - Method not allowed - Does not allow the method you request
- 404 - Page Not Found
- 500 - Internal Service Error
- 503 - Service Unavailable

## Headers
- These are additional bits of data that you can send to the web server when making requests
- They are not required, however limit greatly HTTP requests.
- Common Request Headers are:
  - Host: The host that you want to access within an domain inside a webserver
  - User-Agent - Your browser software and version number, telling the web server your browser software helps it format the website properly
  - Content-Length
  - Accept-Encoding - Tells the web server what types of compression methods the browser supports so the data can be made smaller for transmitting over the internet
  - Cookie - Data sent to the server to help remember your information
 
- Common Response Headers
   - Set-Coookie - Information to store which gets sent back to the web server on each request
   - Cache-Control - How long to store the content of the response in the browser cache
   - Content-Type - The type of data that is being returned
   - Content-Encoding - Method of compression
 
## Cookies
- They are set with Set Cookie header. When stored, every further request, until expiration, to a webserver, will send the cookie data back to the web server.
- HTTP is stateless, so cookies serve to remind the web server who you are, personal settings, or if you have already visited the website.
