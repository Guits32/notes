
### Plan de Fred

Si tu a qu un seul noeud proxmox
Tu monte deux vmbr
Le vmbr0 bridge sur ton interface réseau physique
L autre bridge sur une interface virtuelle
Tes VM tu les déploie sur le vmbr1
Opensense aura le wan sur vmbr0
Et le lan sur le vmbr1
Après sur le noeud proxmox tu fais des iprules pour drop tout le traffic sur le 8006 22 si il ne vient pas de ton lan de ta box ou de la range de ton vpn 
Typiquement le 192.168.0.0/24 je crois
Ça sera deja pas mal
Et si tu es a l aise tu fais des ip rules pour bloquer tout traffic de ton vmbr1 vers le vmbr0 si il ne passe pas par ton pfsense
Concernant le rasp si c'est un gros ça peut le faire

### Ce que j'avais écris

Le plan doit être construit en 2 parties:
- mettre en place un firwall puis ouvrir la dmz de la box - voir les impacts
- une fois valider que le firewall est opérationnel, mise en place du VPN
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