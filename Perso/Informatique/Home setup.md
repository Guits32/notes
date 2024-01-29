
## Mise en place d'un Proxmox

Tuto proxmox + pfsense:

Partie 1: [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/)
Partie 2: [là](https://blog.zwindler.fr/2020/03/09/proxmox-ve-6-pfsense-sur-un-serveur-dedie-2-3)

### Mise en place du PFSense

Repoussé à plus tard, car plutôt complexe et pas le temps de monter en compétence sur tous les sujets en //.**n**
### Setup d'un relay SMTP

- [ ] une fois le nom de domaine transférable depuis domain.com vers scaleway, suivre ce tuto pour cabler le postfix du PVE vers un relais smtp - [tuto](https://www.scaleway.com/en/docs/tutorials/configure-smtp-relay-tem/)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec ssh - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#le-serveur-ssh)
	- [ ] tester que le fail2ban envoit des mails en cas de trop nombre echec de connexion à l'interface proxmox - cf les règles définies [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/#retour-sur-fail2ban)

### Mise en place d'un VPN

#### Mise en place d'un dynamic DNS

Le DNS dynamique va permettre de mapper une IP dynamique (celle de la box) sur un domaine statique, ainsi on peut me connecter au VPN en utilisant des informations qui ne changeront pas (ou en tout cas, pas parce que l'IP a changé).

**Ca devient intéressant à partir du moment où j'aurai installé un VPN. Tant que je n'ai pas de VPN, aucun intérêt à faciliter l'accès au réseau local.**

A voir si scaleway propose une offre de dynDNS (ticket [ici](https://console.scaleway.com/support/tickets/500W5000000u34sIAA)), sinon il existe des offres gratuites en ligne (liste comparative [ici](https://www.ionos.com/digitalguide/server/tools/free-dynamic-dns-providers-an-overview/)). Et sinon OVH propose ça en plus d'un relais mail, donc peut être à voir.

#### Mise en place d'un VPN

Rien regardé pour le moment