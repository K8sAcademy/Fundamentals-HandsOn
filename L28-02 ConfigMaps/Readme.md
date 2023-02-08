# L28-02

## Create the ConfigMap

    kubectl apply -f cm.yaml

## Get the ConfigMap info

    kubectl get cm
    kubectl describe configmap cm-example

Let's output the same information in YAML format

    kubectl get configmap cm-example -o YAML

## Deploy the pod

    kubectl apply -f pod.yaml

## Connect to the Busybox

    kubectl exec mybox -it -- /bin/sh

## Display the CITY env variable

    echo $CITY
    exit

## Cleanup

    kubectl delete -f cm.yaml
    kubectl delete -f pod.yaml --grace-period=0 --force