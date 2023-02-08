# L07-02

This time, we'll containerize an .NET Core app.

## Generate the project

The project is already located in the lab's folder.  It was created using this command:

    dotnet new webapp

## Build the image

The Dockerfile is already created.

In the terminal, type the following commands:

    docker build -t dotnetwebapp:latest .

## Run an instance

    docker run -d -p 8080:5289 --name webapp dotnetwebapp:latest

## List the containers running

    docker ps

## Display using the app

Point your browser to http://localhost:8080

## Cleanup

    docker stop webapp
    docker rm webapp
    docker rmi dotnetwebapp:latest
