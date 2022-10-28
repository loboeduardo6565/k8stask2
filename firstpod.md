### Para la realización de esta actividad se preparó un entorno en Vagrant con Ubuntu 20.04

#### 1.- Se crea un archivo yaml con la descripción del recurso Pod : challenge.yaml


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

#### 2.- Se crea el pod: 

![image](https://user-images.githubusercontent.com/67799058/198461569-29ce6210-4418-488f-9d32-14cdd4c7fe21.png)

#### 3.- Se verifica el estado del pod:

![image](https://user-images.githubusercontent.com/67799058/198462451-e67b3d91-8b14-4c7f-82fb-09801b22d27a.png)

#### 4.- Se muestra la información detallada del pod: 

![image](https://user-images.githubusercontent.com/67799058/198462905-45e55e87-0f50-4f47-bfb3-dc0ce1508380.png)

#### 5.- Se accede de forma interactiva al pod y se muestran los archivos dentro de la ruta /usr/local/apache2/htdocs/

![image](https://user-images.githubusercontent.com/67799058/198463751-4053a3f5-709f-4f89-8871-addfd81df2d1.png)

#### 6. Se crea una redirección al puerto 8080

```
Antes de eso se configura el forwarded_port desde Vagrant

config.vm.network "forwarded_port", guest: 8080, host: 8080
```

![image](https://user-images.githubusercontent.com/67799058/198466297-7f88ffed-d84a-409f-88fa-f2761261d93d.png)


#### Se instala Lynx para consultar el servicio web

![image](https://user-images.githubusercontent.com/67799058/198465831-6d0ad40d-4316-4891-8e58-fca13c9825e5.png)

#### 7. Se muestran los logs y se observan las consultas al servicio web. 

![image](https://user-images.githubusercontent.com/67799058/198467007-a08ff1cc-099e-4e83-9f31-3d109abc12e9.png)

#### 8. Se elimina el pod

![image](https://user-images.githubusercontent.com/67799058/198467968-dcb65a24-7e25-4522-a980-f8eb493b8404.png)

