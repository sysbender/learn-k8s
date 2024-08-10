
https://hub.docker.com/u/richardchesterwood



```shell
kubectl get all
minikube ip
kubectl describe pod webapp

 kubectl exec webapp hostname
 kubectl -it exec webapp sh

# describe with kind
kubectl describe service fleetman-webapp
# show pods with label
kubectl get pods --show-labels
# filter by label
kubectl get pods --show-labels -l release=0

```

### pod label
* Pod label : key-value pairs
* service selector: key-value pairs  




