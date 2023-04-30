#If you wish, you can set an appropriate hostname for each node.
##On the control plane node:
```
sudo hostnamectl set-hostname k8s-control
```
##On the first worker node:
```
sudo hostnamectl set-hostname k8s-worker1
```
##On the second worker node:
```
sudo hostnamectl set-hostname k8s-worker2
```
# On all nodes, set up the hosts file to enable all the nodes to reach each other using these hostnames.
```
sudo vi /etc/hosts
```

On all nodes, add the following at the end of the file. You will need to supply the actual private IP address for each node.
```
{
<control plane node private IP> k8s-control
<worker node 1 private IP> k8s-worker1
<worker node 2 private IP> k8s-worker2
}
```
Log out of all three servers and log back in to see these changes take effect.
  
# The execute the common.sh file on all nodes
# Execute Master.sh on master node
```
sudo kubeadm token create --print-join-command
```
#run above on master node 
it will give an o/p like kubeadm join ...

# Run that on all worker nodes

#Also to install k9s, run the below cmd

```
curl -sS https://webi.sh/k9s | sh
```



