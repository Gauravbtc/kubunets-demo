# Create POD in Kubernets
## Steps 
- Create yaml file Pod.yaml in your project dir
```yaml
apiVersion: v1
kind: Pod
metadata: 
  name: nginx
  labels: 
    app: nginx
    tier: frontend
spec:
  containers:
  - name: nginx
    image: nginx
```
or you can copy code from pod.yml file 

- Create Deployment
```
kubectl create -f pod.yaml
```

- Check Pods 
```
kubectl get pods 
```

if it's shows above output then nginx pod is created.

## To get more details about pods 
```
kubectl describe pod nginx
```
