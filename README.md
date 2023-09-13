# recipe-app-api
Recipe API project built with Django

# Course notes

## What is a Dockerfile?
It's a text document that contains all the commands necesary to assemble a Docker image. List of steps for creating image:
* Choose a base image (e.g: python)
* Install dependencies
* Setup users

## What is Docker Compose?
It's a tool for defining and running multi-container Docker applications. Defines how our Docker images should be used. Each image is defined as a "service" with:
* Name (e.g: app)
* Port mappings
* Volume mappings

### How to run commands through Docker Compose

```
docker-compose run --rm app sh -c "python manage.py collectstatic"
```
* run: start a specific container defined in config
* --rm: removes the container
* sh -c: passes in a shell command

```
docker-compose run --rm app sh -c "flake8"
docker-compose run --rm app sh -c "django-admin startproject app ."
```

## How to run application
```
docker-compose up
```