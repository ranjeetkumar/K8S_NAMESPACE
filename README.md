gcloud container clusters get-credentials my-cluster --zone us-central1-a
kubectl create namespace dev
kubectl create namespace prod
kubectl get namespaces
kubectl apply -f nginx-dev.yaml
kubectl apply -f nginx-prod.yaml
kubectl get deployments -n dev
kubectl get deployments -n prod
kubectl apply -f nginx-service-dev.yaml
kubectl apply -f nginx-service-prod.yaml
kubectl get services -n dev
kubectl get services -n prod
kubectl apply -f resource-quota-dev.yaml
kubectl get resourcequota -n dev


