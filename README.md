This Repository is to implement Blue-green Deployments in Kubernetes.
- Create Configmap files using the below commands.

```sh
   Kubectl apply -f index-html-configmap-blue.yaml
```
```sh
   Kubectl apply -f index-html-configmap-green.yaml
```

- Create a deployment for  version 1 of the app by using the below caoomands
```sh
   Kubectl apply -f blue-deployment.yaml
```
- create a service using the below command 
```sh
   kunectl apply -f nginx-blue-green-service.yaml
```
- Aceess the service using http://localhost:9000/

- Create a green Deployment i.e., version 2 of the app using below command
```sh
Kubectl apply -f green-deployment.yaml
```

- Open  the service file nginx-blue-green-service.yaml and chenge the line no 8  app: nginx-green and reapply the changes using below command
```sh
kunectl apply -f nginx-blue-green-service.yaml
```

- Aceess the service using http://localhost:9000/

-Now the new version of the app will be displayed.
