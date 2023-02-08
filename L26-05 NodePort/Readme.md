# L26-05

Let's expose a deployment using a Nodeport service.

## Deploy the app

    kubectl apply -f deploy-app.yaml

## Deploy the NodePort service

    kubectl apply -f nodeport.yaml

## Get the pods list

    kubectl get pods -o wide

## Use the nodeport

Since we are using Docker Desktop and that the Docker Desktop node is mapped to localhost, to reach the service you need to use **localhost** + the **nodeport**.

When using a Cloud provider, you would need to get a node IP address instead of localhost.

Get the node public IP address

    kubectl get nodes -o wide

## Cleanup

    kubectl delete -f nodeport.yaml
    kubectl delete -f deploy-app.yaml
