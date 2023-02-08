# L30-04

K9s is a great dashboard running in a terminal.

    https://k9scli.io/

## Install K9s

Install it on:

Windows (if you have Chocolatey installed):

    choco install k9s

macOS (if you have Brew installed):

    brew install k9s

Linux: see https://k9scli.io/topics/install/


## Create a deployment and watch what's happening in the Dashboard

    kubectl create -f hello-deployment.yaml

## In a new terminal, launch K9s

    K9s

Watch what's happening in K9s

## Delete a pod

Select one of the pods and delete it by typing **Ctrl-k**.  You'll notice that the pod will be replaced almost immediately.

## Cleanup

    kubectl delete -f hello-deployment.yaml