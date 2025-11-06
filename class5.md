# Introduction to Docker

* Docker is a platform for creating and managing containers
* It packages an application with all its dependencies so it runs the same everywhere

## Containers
* Lightweight and portable
* Include app, runtime, libraries, and settings
* Share host OS kernel (lighter than virtual machines)

## Images
* Read-only templates
* Used to create containers
* Contain application and dependencies

## Docker Daemon
* Background service running on host
* Manages containers, images, networks, and volumes

## Docker Client
* Command-line tool (CLI)
* Sends commands to Docker daemon
* Can connect to local or remote daemon

# Volumes & Networking

## Volumes
* Provide persistent storage
* Data remains even if container is removed

## Networking
* Enables container-to-container communication
* Allows access to external systems


# Working with Docker

## Running Containers
* Use `docker run` command
* `-i` → interactive
* `-t` → terminal access

## Docker Hub
* Cloud-based image repository
* Default source for Docker images

