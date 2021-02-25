Docker Unix installation:

## Docker for Linux Setup and Tips

curl -fsSL get.docker.com -o get-docker.sh

sh get-docker.sh

sudo usermod -aG docker bret

docker version

curl -L https://github.com/docker/compose/releases/download/1.15.0/docker-compose- `uname -s `- `uname -m` >/usr/local/bin/docker-compose

docker-compose version

----------------------------------------------------------------------------------------------

##Docker Commands:
----------------------------------------------------------------------------------------------------------------------------------------------

Docker Info:

This command displays system wide information regarding the Docker installation. Information displayed includes the kernel version, number of containers and images.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
docker container run --publish 80:80 --detach nginx

To start the container from nginx image and publishing or exposing it from 80 port
---------------------------------------------------------------------------------------------------------------

docker container stop 690

Stoping the container by using last three numbers from container name
----------------------------------------------------------------------------------------------------

docker container ls

This will list the running containers.
------------------------------------------------------------------------------------------------

docker container ls -a

Above will list the running container and stopped container and exited containers.
-----------------------------------------------------------------------------------------------------------------------

docker container run --publish 80:80 --detach --name webhost nginx

Above will start the nginx container (once downloaded from hub registry) with the  name webhost in detach mode
--------------------------------------------------------------------------------------------------------------------------------------------------
docker container logs webhost

Above will give us the continer logs.
--------------------------------------------------------------------------

docker container top webhost

Display the running processes of a container

From <https://docs.docker.com/engine/reference/commandline/top/> 
-----------------------------------------------------------------------------------------------------------------------

docker container rm 63f 690 ode

Removing the stopped containers with last three digits of name of the container. 

----------------------------------------------------------------------------------------------------

docker container rm -f 63f

Removing the running containers forcefully.
----------------------------------------------------------------------------------------------

docker run --name mongo -d mongo

docker ps

The docker ps command only shows running containers by default. To see all containers, use the -a (or --all) flag:

From <https://docs.docker.com/engine/reference/commandline/ps/> 

------------------------------------------------------------------------------------------------------------------------

docker top mongo

Above will shows running process in container.
-----------------------------------------------------------------------------------

docker stop mongo

To stop Container
-----------------------------------------------
docker start mongo

To start the container.
-------------------------------------------------------










