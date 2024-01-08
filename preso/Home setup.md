Tuto proxmox + pfsense:

```
https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/
```

A faire:

- Mettre en place le DynDNS et faire une entrée pour l'interface du  proxmox
- Configurer un serveur de mail
- Configurer le postfix de la VM proxmox pour qu'il envoie des mails sur le serveur de mail

## Mise en place d'un dynamic DNS

Le DNS dynamique va permettre de mapper une IP dynamique (celle de la box) sur un domaine statique, ainsi je pourrai me connecter au VPN en utilisant des informations qui ne changeront pas (ou en tout cas, pas parce que l'IP a changé).

**Ca devient intéressant à partir du moment où j'aurai installé un VPN. Tant que je n'ai pas de VPN, aucun intérêt à faciliter l'accès au réseau local.**

Le DynDNS est un service externe au réseau de ce que j'ai compris, il y en a des gratuits, par exemple [no-ip](https://www.noip.com/)
## Mise en place du serveur mail

Pour pouvoir mettre en place en place le serveur mail sur le proxmox, il faut que la VM soit exposé sur le NET a priori. Ce tutoriel semble pas mal: https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-as-a-send-only-smtp-server-on-ubuntu-22-04

Je pense également que pour utiliser le protocole 587 et être en mode "sécurisé" il faut mettre en place un certificat tls qui sera utilisé par le postfix.

Pour la VM de mail les specs hardware nécessaire (avec un debian server):
- disk: 3 GB
- RAM: 512 MB
- CPU: 1 thread