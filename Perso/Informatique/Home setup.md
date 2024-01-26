
## Mise en place d'un Proxmox

Tuto proxmox + pfsense:

```
https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/
```

### Setup d'un relay SMTP

- [ ] une fois le nom de domaine transférable depuis domain.com vers scaleway, suivre ce tuto pour cabler le postfix du PVE vers un relais smtp - [tuto](https://www.scaleway.com/en/docs/tutorials/configure-smtp-relay-tem/)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec ssh - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#le-serveur-ssh)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec de connexion à l'interface proxmox - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#retour-sur-fail2ban)

### Mise en place d'un VPN

#### Mise en place d'un dynamic DNS

Le DNS dynamique va permettre de mapper une IP dynamique (celle de la box) sur un domaine statique, ainsi on peut me connecter au VPN en utilisant des informations qui ne changeront pas (ou en tout cas, pas parce que l'IP a changé).

**Ca devient intéressant à partir du moment où j'aurai installé un VPN. Tant que je n'ai pas de VPN, aucun intérêt à faciliter l'accès au réseau local.**

A voir si scaleway propose une offre de dynDNS, sinon il existe des offres gratuites en ligne.
## Mise en place du serveur mail

Pour pouvoir mettre en place en place le serveur mail sur le proxmox, il faut que la VM soit exposé sur le NET a priori. Ce tutoriel semble pas mal: https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-as-a-send-only-smtp-server-on-ubuntu-22-04

Je pense également que pour utiliser le protocole 587 et être en mode "sécurisé" il faut mettre en place un certificat tls qui sera utilisé par le postfix.

Pour la VM de mail les specs hardware nécessaire (avec un debian server):
- disk: 3 GB
- RAM: 512 MB
- CPU: 1 thread