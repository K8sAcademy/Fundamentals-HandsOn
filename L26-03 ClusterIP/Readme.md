# L26-03

## Deploy the service

    kubectl apply -f clusterip.yaml

## Deploy the app

    kubectl apply -f deploy-app.yaml

## Deploy Busybox

    kubectl apply -f pod.yaml

## Get the pods list

    kubectl get pods -o wide

## Connect to the BusyBox container

    kubectl exec mybox -it -- /bin/sh

## Get the Nginx home page thru the ClusterIP service

    wget -qO- http://svc-example:8080
    exit

## Cleanup

    kubectl delete -f clusterip.yaml
    kubectl delete -f deploy-app.yaml
    kubectl delete -f pod.yaml --grace-period=0 --force