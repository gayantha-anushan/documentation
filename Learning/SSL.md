# Web Security - 1
### SSL
SSL Stands for secure socket layer.older security protocol that no longer use itself.but it laid the current stand TLS (Transport Layer Security ). both SSL and TLS encrypt data transfered between web server and browser
### How it works
1. encryption : uses encryption algorithm to hide the data
2. authentication  : SSL | TLS certificates verify identity of web.

Data Integrity helps to ensure that data hasn't  been tempered with during transfer.

### HTTPS (Hyper Text Transfer Protocol Secure)
##### what http do
1. protect privacy
2. secure online transaction
3. build trust

##### https importance
- for share personal info

### configure https
#### obtain SSL | TLS Certificate
there are 2 ways 
1. free
2. paid
#### configure web server
configuring process of web server is depend on web server provider
#### update website link
update links to use https
#### self signed certificates
1. certificate created by user
2. web browsers are not trust
3. it's guidable to internet use
4. Trust can manually install. but it's not public solution.
### CA Certificates
Trust certificate authority
##### Built-in Trust
every browsers comes with pre installed trusts. these certificates are act as foundation of trust for entire trust. this certificates called trusted root certificates.
##### Certificate Validation
- certificate contains info about web and digital sign of issuing CA. this called certificate chain verification.
- browser verify certificate valid details. this called certificate validity
- sometimes CA Revoke certificate. because of security. so browser check it also.
