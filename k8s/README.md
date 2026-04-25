## ☸️ Kubernetes Deployment

This project can be deployed using Kubernetes in the `dg-survey` namespace.

### 1. Create namespace

```bash
kubectl create namespace dg-survey

---
Deploy application

kubectl apply -n dg-survey -f k8s/

---

Check resources

kubectl get all -n dg-survey
