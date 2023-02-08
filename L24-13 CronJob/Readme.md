# L24-13

Let's now use the CronJob template.

## Create the Job

    kubectl apply -f cronjob.yaml

## Get the jobs list

    kubectl get cronjobs

## Get more info

    kubectl describe cronjob

## Get the pod name

Get the pod's log.  Something starting with **hello-**

    kubectl get pods

## Get the jobs list

Get the container's log.  You should see **Hello from the Job**.

    kubectl logs <podName>

## Cleanup

    kubectl delete -f cronjob.yaml