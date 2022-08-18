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

![Nginx Pod](https://user-images.githubusercontent.com/16643699/185358843-35740704-363a-4b53-8ff6-cc47f4144b73.png)

if it's shows above output then nginx pod is created.

## To get more details about pods 
```
kubectl describe pod nginx
```
