# docker-trails
Docker, Docker Hub, Ngnix, Let's Encrypt, Docker-gen, Triple Triad.. An Adventure


##Docker
Docker containers wrap up a piece of software in a complete filesystem that contains everything it needs to run: code, runtime, system tools, system libraries – anything you can install on a server. This guarantees that it will always run the same, regardless of the environment it is running in.

```bash
#aggregates the output of each container
docker-compose up
```

List containers and show container logs:

```bash
#List containers
docker ps
#List all containers
docker ps -a
#View log
docker logs <container id>
```

Stopping containers, deleting containers and images:

```bash
#Stop all containers
docker stop $(docker ps -a -q)
#Delete all containers
docker rm $(docker ps -a -q)
#Delete all images
docker rmi $(docker images -q)
```

Reset

```bash
docker-machine restart default
eval $(docker-machine env default)
```

##Docker Hub
Host docker images for the community much like github hosts repositories.

As an example to get the latest docker image for ngnix issue the following command: 
```docker pull jwilder/nginx-proxy```

##Nginx-proxy = Ngnix + docker-gen
[ngix-proxy](https://github.com/jwilder/nginx-proxy) sets up a container running nginx and docker-gen. docker-gen generates reverse proxy configs for nginx and reloads nginx when containers are started and stopped.


##Let's Encrypt
[Let's Encrypt](https://letsencrypt.org/) is a free, automated, and open certificate authority. Let’s Encrypt automates away the pain and lets site operators turn on and manage HTTPS with simple commands.
