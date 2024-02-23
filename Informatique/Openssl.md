Generate an rsa key:
```
openssl genrsa -out ca.key 2048
```

Create a certificate signing request (csr):
```
openssl req -new -key foo.key -subj "/CN=toto/O=titi" -out foo.csr
```

If it's a self signed certificate and I have the CA key and certificate, I can sign it an generate the certifacte like so:
```
openssl x509 -req -in foo.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out foo.crt -days 1000
```

