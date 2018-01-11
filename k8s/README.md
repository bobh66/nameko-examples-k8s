# TODO: Add tutorial here

```sh
$ make deploy-chart
helm upgrade gateway charts/gateway --install \
	--namespace=examples --kube-context=minikube \
	--set image.tag=latest
Release "gateway" has been upgraded. Happy Helming!
LAST DEPLOYED: Thu Jan 11 14:07:31 2018
NAMESPACE: examples
STATUS: DEPLOYED

RESOURCES:
==> v1/Service
NAME     TYPE       CLUSTER-IP  EXTERNAL-IP  PORT(S)  AGE
gateway  ClusterIP  10.0.0.131  <none>       80/TCP   2s

==> v1beta2/Deployment
NAME     DESIRED  CURRENT  UP-TO-DATE  AVAILABLE  AGE
gateway  1        1        1           0          2s

==> v1beta1/Ingress
NAME     HOSTS  ADDRESS  PORTS  AGE
gateway  *      80       2s


NOTES:
Thank you for installing Gateway Service!
```


```sh
$ helm list
NAME    	REVISION	UPDATED                 	STATUS  	CHART           	NAMESPACE
broker  	1       	Wed Jan 10 16:08:07 2018	DEPLOYED	rabbitmq-0.5.3  	examples
cache   	1       	Wed Jan 10 16:12:02 2018	DEPLOYED	redis-0.7.1     	examples
db      	1       	Wed Jan 10 16:00:23 2018	DEPLOYED	postgresql-0.7.1	examples
gateway 	2       	Thu Jan 11 14:07:31 2018	DEPLOYED	gateway-0.1.0   	examples
orders  	2       	Thu Jan 11 14:46:27 2018	DEPLOYED	orders-0.1.0    	examples
products	1       	Thu Jan 11 14:47:39 2018	DEPLOYED	products-0.1.0  	examples
```
