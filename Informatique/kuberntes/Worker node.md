## SWAP

For matter of memory handling the SWAP must be off on wor'ker node. See this enhancement for further info: https://github.com/kubernetes/enhancements/tree/master/keps/sig-node/2400-node-swap

To disable the swap in the current session:
```
sudo swapoff -a
```

To disable the swap at startup:
```
sudo sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab
```