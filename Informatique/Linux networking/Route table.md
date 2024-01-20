Lister les entrées dans la table de routage de l'hôte:
```
sudo route
```

(éphémère) - Ajouter une entrée dans la table de la table de routage de l'hôte :
```
sudo ip route add 192.168.1.0/24 via 192.168.15.1
```

(éphémère) - Supprimer une entrée dans la table de routage de l'hôte:
```
sudo ip route del 192.168.1.0/24
```
