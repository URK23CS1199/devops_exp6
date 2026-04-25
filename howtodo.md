# Install Minikube
winget install minikube

# Install Kubectl
winget install Kubernetes.kubectl
or 
kubectl config use-context docker-desktop

# Step 1 – Create a deployment

kubectl create deployment myapp --image=nginx:latest
kubectl get deployments
kubectl get pods


# Step 2 – Scale the deployment

kubectl scale deployment myapp --replicas=3
kubectl get pods

kubectl scale deployment myapp --replicas=1


# Step 3 – Expose, inspect & clean up

kubectl expose deployment myapp --port=80 --type=NodePort
kubectl get services
kubectl describe pod <pod-name>
kubectl logs <pod-name>

kubectl delete deployment myapp
kubectl delete service myapp
