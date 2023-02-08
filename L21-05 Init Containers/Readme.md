# L21-06

Let's use an Init container.

## Create the deployment

    kubectl apply -f myapp.yaml

Wait for the main pod to come up

    kubectl get pods

## Connect to the Nginx container

    kubectl exec -it init-demo -- /bin/bash

## Hit the default webpage

It should be the one downloaded by the Init container from http://info.cern.ch

    curl localhost
    exit

## Cleanup

    kubectl delete -f myapp.yaml