### Certificats SSL
- synchroniser les tabs tmux: `[crtl-b]` => `:setw synchronize panes`
- décoder un fichier `.csr`:
```bash
openssl req -in file.csr -text -noout
```
- décoder un fichier `.crt`
```bash
openssl x509 -in file.crt -text -noout
```
- indenter un fichier dans Vim: `gg=G`
- retourner à l'explorateur de fichier de Vim: `:E`
- installer les paquets:
	- `arp`, `netstat`, `route` => `sudo apt install net-tools`
	- `dig`, `nslookup` => `sudo apt install dnsutils`
	- `nc` => `sudo apt install netcat`
