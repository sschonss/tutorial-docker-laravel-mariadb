# Docker & Laravel
## _Laravel + MariaDB_
---

# Introduction :page_facing_up:

This tutorial will help you to create a Laravel project using Docker.

My goal is to help you to create a Laravel project using Docker in a simple way.

I decided write this tutorial because I had some difficulties to create a Laravel project using Docker and I want to help you to avoid these difficulties.

If you have any questions, you can contact me on [LinkedIn](https://www.linkedin.com/in/luiz-schons/) or [GitHub](https://github.com/sschonss).

>That is my first tutorial in English, sorry for any mistakes.

---
# Installation :whale:

## Docker
- [Docker](https://docs.docker.com/get-docker/)

For Windows, you need to install [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and [Docker Desktop](https://docs.docker.com/docker-for-windows/install/)

## Docker Compose
- [Docker Compose](https://docs.docker.com/compose/install/)
---

# Usage :rocket:

## Clone the docker-compose.yml file
```sh
mkdir ~/myapp && cd ~/myapp
curl -LO https://raw.githubusercontent.com/bitnami/containers/main/bitnami/laravel/docker-compose.yml
```

## Attention :warning:

You need to change environment variables in the docker-compose.yml file to your own values.

Sometimes, you need to change the ports in the docker-compose.yml file to avoid conflicts with other services.

Maybe you need open you project `~/myapp` in your IDE or text editor to edit your .env file.

Remember to change the DB_HOST variable in your .env file to the name of the service defined in the docker-compose.yml file.

Could be necessary change permissions of the `~/myapp` directory, because the container will create files in this directory and maybe you can't edit these files.



## Start the services :muscle:
```sh
docker-compose up
```

One tip: You can use the -d flag to run the containers in the background:
```sh
docker-compose up -d
```

I recommend you don't use the -d flag when you start the containers for the first time, because you can see the logs of the containers and check if everything is working correctly.

## Stop the services :stop_sign:
```sh
docker-compose down
```

## Tips :bulb:

### Check the status of the containers
```sh
docker-compose ps
```

### Check the logs of the containers
```sh
docker-compose logs
```

### Check the logs of a specific container
```sh
docker-compose logs <container-name>
```

### Check the logs of a specific container in real time
```sh
docker-compose logs -f <container-name>
```

## Access the application :computer:

In your terminal, you can see the URL of your application.

Normally, the URL is http://localhost:8000 if you don't change the ports in the docker-compose.yml file.

## Access the database :floppy_disk:

I recommend you use [DBeaver](https://dbeaver.io/) or [DataGrip](https://www.jetbrains.com/datagrip/) to access the database.

You can use the credentials defined in the docker-compose.yml file.

## Access the container :package:

You can access the container using the following command:
```sh
docker-compose exec <container-name> bash
```

If you use Windows, you can open Docker Desktop and click in the container name to open a terminal.

## Final considerations :memo:

I recommend you read the [Bitnami Laravel](https://hub.docker.com/r/bitnami/laravel/) documentation to learn more about this image.

You can use this [Bitnami Laravel](https://hub.docker.com/r/bitnami/laravel/) image in production, but you need to change the environment variables in the docker-compose.yml file to your own values.

I wrote this tutorial to help you, but I don't know everything about Docker and Laravel, i'm learning too.

I hope this tutorial helps you. :smile:

[LinkedIn](https://www.linkedin.com/in/luiz-schons/)
[GitHub](https://github.com/sschonss)

---
