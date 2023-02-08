# L24-11

Let's now use the Job template.

## Create the Job

    kubectl apply -f job.yaml

## Get the jobs list

    kubectl get jobs

## Get more info

    kubectl describe job

## Get the pod name

Get the pod's log.  Something starting with **hello-**

    kubectl get pods

## Get the jobs list

Get the container's log.  You should see **Hello from the Job**.

    kubectl logs <podName>

## Cleanup

    kubectl delete -f job.yaml