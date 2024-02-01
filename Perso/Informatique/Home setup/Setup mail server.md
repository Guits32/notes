### Setup d'un relay SMTP

- [ ] une fois le nom de domaine transférable depuis domain.com vers scaleway, suivre ce tuto pour cabler le postfix du PVE vers un relais smtp - [tuto](https://www.scaleway.com/en/docs/tutorials/configure-smtp-relay-tem/)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec ssh - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#le-serveur-ssh)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec de connexion à l'interface proxmox - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#retour-sur-fail2ban)

