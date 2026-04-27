docker container ls -a
docker container run --publish 80:80 --detach --name webhost nginx
docker container ls
docker container stop webhost -- stop the container
docker container logs webhost
docker container top webhost -- processes running in the container
docker container remove webhost
docker container remove -f webhost
docker ps
-e or --env -- set environment variables in the container
docker container inspect ngnix -- inspect the container's configuration and details
docker container stats webhost -- view real-time resource usage statistics for the container (old way)
docker container run -it --name proxy nginx bash -- run a container interactively with a bash shell
docker container exec -it mysql bash -- run additional commands in a running container interactively
docker container start -ai proxy -- start the container and attach to it interactively
docker pull alpine -- pull the alpine image from Docker Hub
docker container inspect --format '{{ .NetworkSettings.IPAddress }}' webhost
--format -- format the output of docker commands using Go templates

docker network ls
docker network inspect bridge -- inspect the default bridge network
docker network create mynetwork -- create a custom network
docker network connect mynetwork webhost -- connect a container to a network
docker network disconnect mynetwork webhost -- disconnect a container from a network
--link -- link containers together (deprecated in favor of user-defined networks)
--rm -- automatically remove the container when it exits

docker image ls -- list all Docker images on the host machine
history -- view command history in the terminal

docker image tag nginx battousai/nginx

docker image build -t name . -- build a Docker image from a Dockerfile in the current directory

ps aux -- processes running on the host machine
ps aux | grep mongo -- grep filters processes by name
