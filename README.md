
# Web Server backend sample code

The code in this repository is piece of a HTTP web server I am currently building,it doesn't prove the HTTP layer yet,
it's a TCP byte stream that easily adapt to any protocol, it has some http-related features like a minimal CGI interface,
while other features are still in development.

### server/

This folder is the entrypoint of the server, it starts by parsing a confguration file, creates the server and starts it.

### net/

This folder contains the networking part of the project, listening sockets and client connections are created here.

### runtime/

This folder abstracts the IO multiplexing and polling mechanism, it uses epoll as the prefered api, but can adapt to others depending on the platform, only the epoll version is available now.

### cgi/

Basic CGI implementation, it essentially parses the CGI output into an HTTP response.

