# Getting logs
1. Before dumping logs you might want to [raise the openshift-sdn loglevel](https://access.redhat.com/solutions/5311361) first. 
2. You create a debug pod with a fedora image on that node `oc debug --image fedora:31 node/<node name>`
3. In a separate terminal session you do: `oc rsync $DEBUG_POD:/host/$LOCATION_ON_NODE $LOCATION_ON_YOUR_LOCAL_MACHINE`
