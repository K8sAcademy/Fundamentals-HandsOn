# L30-03

Lens is a free dashboard app that you can install on Windows, Mac and Linux.

## Install Lens

Directly from the Lens Web site or...

Windows (if you have Chocolatey installed):

    choco install lens

macOS (if you have Brew installed):

    brew install --cask lens

Linux: see https://k8slens.dev/

## Launch Lens

You should be connected to your cluster on (1) Docker Desktop.  If not, you can add it or another cluster by (2) clicking on the **hamburger menu** and (3) **Add Cluster**.

The clusters that are already present in the config file will be listed in the dropdown menu.

Once configured, you should see something like this:


## Deploy the app

    kubectl create -f hello-deployment.yaml

## Lens dashboard

Open the **Workloads** menu and look at the pods, deployments and replications.

## Delete a pod using the UI

Select one of the pods and delete it either by clicking on the (2) **ellipse** icon or the (2) **Delete** icon at the bottom of the screen.  You'll notice that the pod will be replaced almost immediately.

## Open a terminal

At the bottom of the screen, you will see a link called **Terminal**.  Click on it to open the built-in terminal.

## Delete a pod using the terminal

Copy one of the pod name and delete it using the terminal.

    kubectl delete pod [podName]

## Cleanup

    kubectl delete -f hello-deployment.yaml