# L09-05

## Build the app

    docker compose build

## Run the app

    docker compose up -d

This will take a while. When the app will run, launch the app in your browser http://localhost:3000

## List the containers

    docker compose ps

## Look at the backend container logs

    docker compose logs -f backend

Refresh the frontend page a few times, the logs should display each hit

## Stop the app

    docker compose down

## List the containers

Was the app really removed?

    docker compose ps

