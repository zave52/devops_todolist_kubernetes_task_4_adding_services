# Instruction on how to access the app

## Testing app using busybox and calling ClusterIP

### 1. Create namespace

```bash
kubectl apply -f .infrastructure/namespace.yml
```

### 2. Create busybox pod

```bash
kubectl apply -f .infrastructure/busybox.yml
```

### 3. Create todoapp pods

```bash
kubectl apply -f .infrastructure/todoapp-pod.yml
```

### 4. Create ClusterIP service

```bash
kubectl apply -f .infrastructure/clusterIP.yml
```

### 5. Go inside busybox pod

```bash
kubectl exec -it busybox -n todoapp -- sh
```

### 6. Run curl command using ClusterIP DNS name

```bash
curl todoapp-service.todoapp.svc.cluster.local
```
