# Horizontal Pod Autoscaler (HPA)

## What is HPA?
Automatically scales pods based on CPU/memory.

Example trigger:
CPU > 50%

---

## Requirements
Metrics Server must be installed.
CPU requests must be defined.

---

## Flow
1. Metrics Server collects CPU
2. HPA controller evaluates usage
3. Deployment scaled up/down

---

## Commands
```bash
kubectl get hpa
kubectl top pods
kubectl describe hpa
```