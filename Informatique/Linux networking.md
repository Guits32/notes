### Interface réseau

Lister et modifier les interfaces réseau de l'hôte
 ```
ip link
```

Lister les interfaces réseau de l'hôte et les ips associées
```
ip a
```

Ajouter une adresse IP à une interface réseau (seulement valide jusqu'à un redémarrage):
```
ip addr add 192.168.1.10/24 dev eth0
```

Afficher la table de routage de l'hôte:
```
route
```

Ajouter une entrée dans la table de routage
```
ip route add 192.168.1.0/24 via 192.168.2.1
```

Vérifier si l'ip forwarding est activer sur hôte:
```
cat /proc/sys/net/ipv4/ip_forward
```

### DNS resolution

Faire une entrée locale DNS sur l'hôte
```
vim /etc/hosts
```

Lister les serveurs DNS utilisés par l'hôte:
```
cat /etc/resolv.conf
```

Voir ou éditer la configuration de l'ordre des résolutions dns de l'hôte:
```
cat /etc/nsswitch.conf
```

### Network namespaces

Lister les namespace de l'hôte:
 ```
 ip netns
 ```

Créer un namespace sur l'hôte:
```
ip netns add red
```

Exécuter la commande `ip` dans un namespace:
```
ip -n red link
```

Exécuter la commande `arp` dans un namespace:
```
ip -n red arp
```