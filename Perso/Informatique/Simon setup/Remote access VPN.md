Le plan doit être construit en 2 parties:
- mettre en place un firwall puis ouvrir la dmz de la box - voir les impacts
- une fois valider que le 
### Mise en place du PFSense

Tuto proxmox + pfsense:

Partie 1: [ici](https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/)
Partie 2: [là](https://blog.zwindler.fr/2020/03/09/proxmox-ve-6-pfsense-sur-un-serveur-dedie-2-3)

Repoussé à plus tard, car plutôt complexe et pas le temps de monter en compétence sur tous les sujets en //.**n**
### Mise en place d'un VPN

#### Mise en place d'un dynamic DNS

Le DNS dynamique va permettre de mapper une IP dynamique (celle de la box) sur un domaine statique, ainsi on peut me connecter au VPN en utilisant des informations qui ne changeront pas (ou en tout cas, pas parce que l'IP a changé).

**Ca devient intéressant à partir du moment où j'aurai installé un VPN. Tant que je n'ai pas de VPN, aucun intérêt à faciliter l'accès au réseau local.**

A voir si scaleway propose une offre de dynDNS (ticket [ici](https://console.scaleway.com/support/tickets/500W5000000u34sIAA)), sinon il existe des offres gratuites en ligne (liste comparative [ici](https://www.ionos.com/digitalguide/server/tools/free-dynamic-dns-providers-an-overview/)). Et sinon OVH propose ça en plus d'un relais mail, donc peut être à voir.

#### Mise en place d'un VPN

Rien regardé pour le moment