# Deploying a Standalone Application

## Deploying the Application Using the CLI 

- Creating a webserver Deployment:

```
    kubectl create -f webserver.yaml
```

This will also create a ReplicaSet and Pods, as defined:

```
    kubectl get replicasets
```

##

Using kubectl, create the Service:

```
    kubectl create -f webserver-svc.yaml
```

List the Services:

```
    kubectl get svc
```

To get more details about the service:

```
    kubectl describe svc web-service
```

Test the app:

```
    minikube service web-service --url #to get an IP address of the service
    curl http://192.168.99.100:32742
```
