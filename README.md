# Kubernetes Custom Workshoop

In order to complete this trainig you need to have kubectl and minikube installed.

## Kubectl imperative commands:
Using imperative commands you can create and update kubernetes objects in seconds.

## Pods

### Create Pod using imperative way:
```
kubectl run  nginx-deploy --image=nginx 
``` 
You can do the same using declarative way:
```
kubectl apply -f pod.yaml
```
### Generate Pod template
```
kubectl run  nginx-deploy --image=nginx -o yaml --dry-run 
``` 
### Check Pods status, get information about Pods and delete it:
```
kubectl get pods 
kubectl describe pods
kubectl delete pod nginx
``` 

## ReplicaSets
### Create ReplicaSet:
```
kubectl apply -f replicaset.yaml 
``` 
### Get information about replicaset and delete it:
```
kubectl get rs
kubectl delete -f replicaset.yaml
```

##Deployments

### Create Deployment using imperative way:
```
kubectl create deployment nginx-deployment --image=nginx 
``` 
You can do the same using declarative way:
```
kubectl apply -f deployment.yaml
```
### Generate Deployment template
```
kubectl create deployment nginx-deployment --image=nginx  -o yaml --dry-run
``` 

##Services

###Create service using imperative command:
```
kubectl expose deployment nginx-deployment --type=NodePort --port=80
```
You can do the same using declarative way:
```
kubectl apply -f deployment.yaml
```