# Kubernetes Custom Workshoop

In order to complete this trainig you need to have kubectl and minikube installed.

## Kubectl imperative commands:
Using imperative commands you can create and update kubernetes objects in seconds.
### Create pod:
```
kubectl run  nginx-deploy --image=nginx -o yaml --dry-run
``` 
