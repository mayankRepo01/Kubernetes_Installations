# The execute the common.sh file on all nodes
# Execute Master.sh on master node
```
kubeadm token create --print-join-command
```
#run above on master node 
it will give an o/p like kubeadm join ...

# Run that on all worker nodes

#Also to install k9s, run the below cmd

```
curl -sS https://webi.sh/k9s | sh
```



