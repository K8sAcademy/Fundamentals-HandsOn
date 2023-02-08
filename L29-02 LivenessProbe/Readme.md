# L29-02

## Deploy the pod

    kubectl apply -f pod.yaml

## Look at the pod events

    kubectl describe pod liveness-example

## Cleanup

    kubectl delete -f pod.yaml --force --grace-period=0