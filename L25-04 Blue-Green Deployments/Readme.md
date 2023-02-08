# L25-04

**NOTE: If you are running this lab on a ARM64 laptop/PC, edit the YAML file and change the image name from "hello-app" to "hello-arm" keeping the tag name as is.**

## Create a V1 Deployment

    kubectl create -f hello-dep-v1.yaml

## Create the ClusterIP service

    kubectl create -f clusterip.yaml

## Get the pods list

    kubectl get pods -o wide

## Display the app in a browser

First, port forward to the ClusterIP:

    kubectl port-forward service/svc-front 8080:8080

Open a browser and navigate to http://localhost:8080

The app version will be V1.

---

## Create a V2 Deployment

    kubectl create -f hello-dep-v2.yaml

## Get the pods list

    kubectl get pods -o wide

## Edit the ClusterIP manifest

Edit the clusterip.yaml file and change the last line so that the service points to our V2 deployment.

    app: hello-v2

## Update the ClusterIP service

    kubectl apply -f clusterip.yaml

## Display the app in a browser

First, port forward to the ClusterIP:

    kubectl port-forward service/svc-front 8080:8080

Open a browser and navigate to http://localhost:8080

The app version will be V2.

## Cleanup

    kubectl delete -f hello-dep-v1.yaml
    kubectl delete -f hello-dep-v2.yaml
    kubectl delete -f clusterip.yaml