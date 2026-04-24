docker container ls -a
docker container run --publish 80:80 --detach --name webhost nginx
docker container ls
docker container stop webhost
docker container logs webhost
docker container top webhost
docker container remove webhost
docker container remove -f webhost
