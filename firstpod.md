### 1.- Se crea un archivo yaml con la descripción del recurso Pod : challenge.yaml


```
apiVersion: v1
kind: Pod
metadata:
  name: podchall
  labels:
    descripcion: task2
spec:
  containers:
  - name: contchall
    image: roxsross12/k8s_test_web:latest
    ports:
    - containerPort: 80
```

### 2.- Se crea el pod: 

