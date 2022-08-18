# ReplicaSet
A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods.

# How a ReplicaSet works 
[RelplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/)


# Create Replica
## Steps 
- Create yaml file replicaset.yaml in your project dir
```yaml
apiVersion: "apps/v1"
kind: ReplicaSet
metadata: 
  name: replicaset-demo
  labels: 
    app: myapp
spec:
  selector:
    matchLabels:
      app: myapp
  replicas: 2
  template:
    metadata: 
      name: nginx
      labels:   
        app: myapp
    spec:
      containers:
      - name:  nginx
        image: nginx
```
or you can copy code from replicaset.yaml file 

- Create Deployment
```
kubectl create -f replicaset.yml
```
where replicaset.yml is a tenplate to create replicas
- Get repplcasets which you created 
```
kubectl get replicaset 
```
Which get number of replicasets

if it's shows above output then 2 nginx replicas is created.

## Delete any replica
```
kubectl delete replicaset {NameOfReplicaset}
```
## Scale any replica
```
kubectl scale replicaset {NameOfReplicaset} --replicaset={NuberOfInstance}
ex
kubectl scale replicaset replicaset-demo --replicaset=3
```
it will scale replicaset-demo by 3


