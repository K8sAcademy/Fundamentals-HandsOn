# L22-02

## Deploy the app

    kubectl apply -f myapp.yaml

## Deploy the service

    kubectl apply -f myservice.yaml

## Is the service connected to the pod?

If so, the enpoint will point to the pod IP address.  Get the IP address of the pod:

    kubectl get po -o wide

Then get the service endpoint.  The IP address should match.

    kubectl get ep myservice

## Port forward to the service

    kubectl port-forward service/myservice 8080:80

Open a browser and point to http://localhost:8080

Stop the port forward by typing **Ctrl-C**

## Edit the app YAML file

Change the **app** label to myapp2 and save the file

Deploy the change

    kubectl apply -f myapp.yaml

## Check the endpoint again

    kubectl get ep myservice

## Port forward to the service again

    kubectl port-forward service/myservice 8080:80

Open a browser and point to http://localhost:8080

Stop the port forward by typing **Ctrl-C**

## Cleanup

    kubectl delete -f myservice.yaml
    kubectl delete -f myapp.yaml