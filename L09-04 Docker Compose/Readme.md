# L09-04

## Build the app

    docker compose build

## Run the app

    docker compose up -d

When the app will run, launch the voting app in your browser http://localhost:5000


## List the containers

    docker compose ps

## Look at the db container logs

    docker compose logs -f web-fe


## Compose V2 commands

LS will list the current projects

    docker compose ls

## Let's try to deploy a second version

    docker compose up -d

This fails because we can only run an app a single time

## Deploy a second version using a different project name

Let's now use a project name to see if we can deploy a second version

    docker compose -p test up -d

This fails because the localhost port 5000 is already assigned.

Change the ports value from

    - "5000:80"

to

    - "5001:80"

## Deploy again

    docker compose -p test up -d

How many versions do we have running?

    docker compose ls

## Cleanup

    docker compose down
    docker compose ls
    docker compose -p test down
    docker compose ls