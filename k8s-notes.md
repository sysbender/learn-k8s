
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


### depolyment

```shell
kubectl rollout status deployment webapp
kubectl rollout  history deploy webapp


```
### networking

kube-dns
namespace

```shell
kubectl get all -n kube-system

kubectl exec -it webapp-864ddfdb-9nmg7 sh

apk update
apk add mysql-client
mysql -h database -uroot -ppassword fleetman
create table testtable(test varchar(255));
show tables;
```

### full qualified domain name

```ini
/ # cat /etc/resolv.conf
nameserver 10.96.0.10
search default.svc.cluster.local svc.cluster.local cluster.local
options ndots:5
```

default namespace `default.svc.cluster.local`


## microservice



https://github.com/DickChesterwood/k8s-fleetman

clean all: `kubectl delete -f .`

### queue

### position-simulator
env select properties file
`SPRING_PROFILES_ACTIVE=production-microservice`

check log `kubectl logs  position-simulator-74759dfb5f-wq8zv`

* not need service
### position-tracker
rest api: 8080
* /vehicles/{vehicle name}  : City TruCk; City%20Truck
* 'http://192.168.1.100:30020/vehicles/City%20Truck'
env select properties file
`SPRING_PROFILES_ACTIVE=production-microservice`





