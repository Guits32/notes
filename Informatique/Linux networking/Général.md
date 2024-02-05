### IP forward

Vérifier si l'ip forwarding est activer sur hôte:
```
cat /proc/sys/net/ipv4/ip_forward
```

Activer le forward d'ip sur l'hôte:
```
sudo sysctl -w net.ipv4.ip_forward=1
```

To make persistent, edit /etc/sysctl.conf and search for the following lines:

```
# Uncomment the next line to enable packet forwarding for IPv4
#net.ipv4.ip_forward=1
```