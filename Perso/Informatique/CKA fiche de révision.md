### Certificats SSL

- décoder un fichier `.csr`:
```bash
openssl req -in file.csr -text -noout
```
- décoder un fichier `.crt`
```bash
openssl x509 -in file.crt -text -noout
```
