for service webserver-service I have not provided any port, 
to access this service I have to use port which we will get from 
kubectl describe service <svc-name>
NodePort:                 <unset>  31693/TCP
here the value is: 31693
or from 
kubectl get service 
PORT(S)
80:31693/TCP
here the value is: 31693
this is the port of service, to access it we have to get port of node
command to get port of a node
k describe nodes | grep -i address -A 1
output:
Addresses:
InternalIP:  192.168.1.114
I can do:  
curl 192.168.1.114:31693
will get result 
here my pod are running on port: 80
