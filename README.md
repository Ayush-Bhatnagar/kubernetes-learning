# kubernetes-demo
Repo for learning kubernetes. Lets see in action

# Creating a pod using kubectl
kubectl create -f pod.yaml

# Get all the pods
kubectl get pod

# Delete a running pod
kubectl delete pod <pod_name>

# Get all the replicaset
kubectl get replicaset

# Delete a replicaset
kubectl delete replicaset <replicaset_name>

# Describe individual pod
kubectl describe pod <pod_name>

# Deployment

## Change image version in deployment
kubectl set image deployment/helloworld-deployment k8s-demo=arjunachari12/k8s-demo:2

## Rollout Deployment
kubectl rollout status deployment/helloworld-deployment

## Undo Deployment
kubectl rollout undo deployment/helloworld-deployment


## Ingress controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.0.3/deploy/static/provider/cloud/deploy.yaml
minikube addons enable ingress
