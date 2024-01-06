Tuto proxmox + pfsense:

```
https://blog.zwindler.fr/2020/03/02/deploiement-de-proxmox-ve-6-pfsense-sur-un-serveur-dedie/
```

A faire:

- Mettre en place le dynDNS et faire une entrée pour l'interface du  proxmox
- Configurer le postfix de la VM proxmox pour qu'il puisse envoyer des mails

## Mise en place du serveur mail

Pour pouvoir mettre en place en place le serveur mail sur le proxmox, il faut que la VM soit exposé sur le NET a priori.s