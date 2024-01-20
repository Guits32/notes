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
ip netns exec red arp
```

Exécuter la commande `route` dans un namespace:
```
ip netns exec red route
```