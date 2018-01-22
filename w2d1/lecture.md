## HTTP

What happens when...
... you type google.com into the address bar and hit Enter?

Lets talk about the network side of things

#Client (Browser) -> piece of software making request (req);

google.com -> IP address
[--------] -> Domain Name
[----] -> Domain Name
      [--] -> Top Level Domain


mail.google.com
[--] -> Sub-Domain

## Domain name service (DNS) resolution
# 1. Hosts File
File on every OS called the hosts file
hosts = Text file which allows a user to set aliases (domain names) for IP addresses
Mac/Linux - /etc/hosts
first place the computer goes to check

# 2. DNS cache
key value lookup, stored in memory, part of OS, 
key - Domain name
value - Ip address, TTL (Time to Live [expirary])

# 3. IP address source - probably a router or switch
  Also has DNS cache

# 4. ISP - 'internet' service provider
  also has DNS server

# 5. registrar - TLD registrar

# 6. --- n.  Internic the ultimate authority on DNS
  registrar of registrar.

google.com -> 12.34.56.78

http://12.23.45.67
[---] - protocol or scheme
// are separator.

http://12.23.34.45:80
                  [-] - port -> gate or doorway that specificies the address on the machine where the server is listening

"server" -> piece of software listening for an incoming request from a 
"Client" -> which makes request


http://12.23.34.45:80/
                     [] - represents the beginning of the path

the path specifies the resource, all http reqs are for resources, not web page.


## Url / URI

URI - Uniform Resource Indicator
git:git@github.com:/floop.git

URL - Uniform resource locator  - http://12.23.34.56:80/

## Protocol
Standard for how client and server communicate
smtp
ftp
ntp
nntp
http
https
all are standards that set rules for how client and server communicate

uri
-url


## HTTP Request

internet is run on text files
### HTTP verb
the client sending an instruction to the server indicating how the client intends to interact with the resource

GET - fetch a copy of resource
POST - Creating a new resource
PUT - Editing a resource an existing resource, by providing an updated version
PATCH - Editing an existing resource by providing only the changes
DELETE - Destroy an existing resource

client sending instruction indicating how the client aught to do, the server is under no obligation to obey the suggestion.

protocol and version (set standards)


### Header
protocol and version        HTTPv1.1
Verb and PATCH              GET /
Route - uniqu

User-Agent
Cookies

#### Cookies
Just text, stored in key-value format.
to customize requests, modify behaviour or resources

#### Stateless 

HTTP is a stateless protocol. Everything that is needed to satisfy the request must be sent with the request.

every chain can add something to the header of the http request

### Body

GET empty
POST data in Key value pairs

request recieved, servers uses whatever logic it has been provided with to satisfy teh request for the resource

### HTTP response
.txt file

#### HEADER

response code
status message
cookies

## response codes
100 - Informational
200 - Success
300 - Redirection
400 - Client Error 404
500 - Server Error

only see query strings with GET requests

#### Body

Resource (Typically HTML)
network requests are expensive
better alot of js in one file than alot of files with litte js

Resource
(In the case of 300-code, new URL to form a GET)

