# jwt-tutorial
A simple NodeJS tutorial that can be used to create JWT token and send to the client to access protected APIs

In this project, the following things are done:
1. Create a simple REST API using ExpressJS
2. Generate Valid JWTs in NodeJS using a pre-generated private key
3. Create an authorization middleware function that checks incoming requests


To generate the private key:
1. Download openssl by searching in google for "openssl softpedia"
2. Install in a local folder
3. Open a command prompt and type the command 
    > openssl genrsa -out jwt.pem -aes256 -passout pass:password 2048
    
This generates a .pem file that can be used to sign a simple token and send to the caller. Place that file inside the key folder.

Step :0 Try the following URL in postman. Authorization will be denied
http://localhost:3000/secret

Step: 1 To get the JWT token use the following URL (in Postman)
http://localhost:3000/jwt

Step: 2 Now try the following url with the header key named "Authorization" and value "jwt <token>"  
http://localhost:3000/secret
  
The service will be authorized and response will be sent.

Reference:
OpenSSL Step By Step Tutorial | How to Generate Keys, Certificates & CSR Using OpenSSL - https://www.youtube.com/watch?v=wzbf9ldvBjM
Authentication on the Web:  https://www.youtube.com/watch?v=2PPSXonhIck
OAuth 2.0 and OpenID Connect: https://www.youtube.com/watch?v=996OiexHze0
