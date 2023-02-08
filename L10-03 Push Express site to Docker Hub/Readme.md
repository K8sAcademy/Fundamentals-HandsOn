# L10-03

## Docker Hub

Head to https://hub.docker.com and make sure you can log in.

## Add a Dockerfile file

Using the Code tooling, add a new Dockerfile by opening the Command Palette from the View menu.

Type **Docker Add** and select **Docker Add Docker Files to Workspace**.

## Tag using your Docker account name

For the next commands, replace `<YourRegistryName>` with your registry name.

## Build the image

    docker build -t <YourRegistryName>/express:v1 .

## Push the image

    docker push <YourRegistryName>/express:v1

## Docker Hub

Back in hub.docker.com, locate the image you just pushed.

## Pull the image from Docker Hub

Let’s first delete the local image and pull it back from Docker Hub.

## Remove the image

    docker rmi <YourRegistryName>/express:v1

## Pull the image

    docker pull <YourRegistryName>/express:v1

---

## Create version 2

Using the commands you learned earlier, build and push this new version to Docker Hub.

## Build the v2 image

    docker build -t <YourRegistryName>/express:v2 .

## push the image

    docker push <YourRegistryName>/express:v2

## Docker Hub

Back in hub.docker.com, locate the image you just pushed.

## Remove the local image

    docker rmi <YourRegistryName>/express:v2

## Pull the image

    docker pull <YourRegistryName>/express:v1

## Cleanup

    docker rmi <YourRegistryName>/express:v1
    docker rmi <YourRegistryName>/express:v2