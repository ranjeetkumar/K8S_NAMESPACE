# Kubernetes and GKE Setup

## Step 1: Get credentials for the cluster
```bash
gcloud container clusters get-credentials my-cluster --zone us-central1-a
```

## Step 2: Create namespaces
```bash
kubectl create namespace dev
kubectl create namespace prod
```

## Step 3: Verify namespaces
```bash
kubectl get namespaces
```

## Step 4: Apply deployments
### Apply Nginx deployment to `dev` namespace
```bash
kubectl apply -f nginx-dev.yaml
```

### Apply Nginx deployment to `prod` namespace
```bash
kubectl apply -f nginx-prod.yaml
```

## Step 5: Verify deployments
### Check deployments in `dev` namespace
```bash
kubectl get deployments -n dev
```

### Check deployments in `prod` namespace
```bash
kubectl get deployments -n prod
```

## Step 6: Apply services
### Apply service for `dev` namespace
```bash
kubectl apply -f nginx-service-dev.yaml
```

### Apply service for `prod` namespace
```bash
kubectl apply -f nginx-service-prod.yaml
```

## Step 7: Verify services
### Check services in `dev` namespace
```bash
kubectl get services -n dev
```

### Check services in `prod` namespace
```bash
kubectl get services -n prod
```

## Step 8: Apply resource quota for `dev` namespace
```bash
kubectl apply -f resource-quota-dev.yaml
```

## Step 9: Verify resource quota
```bash
kubectl get resourcequota -n dev
```



