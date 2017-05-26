
> Trouble shooting openshift environment.  


### If master is not responding
#### non-HA environment
```sh
systemctl restart etcd #on masters
systemctl restart atomic-openshift-master  #on master
systemctl restart atomic-openshift-node  #on nodes
```
#### HA environment
```sh
systemctl restart etcd #on masters
systemctl restart atomic-openshift-master-api  #on all masters
systemctl restart atomic-openshift-master-controllers  #on all masters
systemctl restart atomic-openshift-node  #on nodes
```

### If router is not working
1. check if your router pod is running on right node 
2. your router should run on same node where you have pointed your wilcard dns.
3. if router pod is running on a wrong node, use nodeSelector point your router pod on right node.


### If registry is not working
1. check if your registry storage is runnign our ot of disk `oc get events -n default`
2. is your registry pod running in `default` namespace.?
