# L24-07

Let's deploy a Busybox as a DaemonSet.

## Create the Deployment

    kubectl apply -f daemonset.yaml

## Get the pods list

There should be one for each worker node.

    kubectl get pods --selector=app=daemonset-example -o wide

## Cleanup

    kubectl delete -f daemonset.yaml