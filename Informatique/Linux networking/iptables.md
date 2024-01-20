Lister les règles de la table `nat`:
```
iptables -t nat -L
```

Ajouter une entrée MASQUERADE:
```
iptables -t nat -A POSTROUTING -s 192.168.15.0/24 -j MASQUERADE
```
