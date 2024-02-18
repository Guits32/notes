## SWAP

**In case the control plane node use kebelet to run control planbe component (kube-apiserver, etcd, controller-manager)**. 

For matter of memory management, the SWAP must be turn off. See this enhancement for further info: https://github.com/kubernetes/enhancements/tree/master/keps/sig-node/2400-node-swap

To disable the swap in the current session:
```
sudo swapoff -a
```

To disable the swap at startup:
```
sudo sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab
```