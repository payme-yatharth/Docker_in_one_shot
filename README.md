# Docker_in_one_shot
This is a repo that is nothing but a semblance of the learnings from the piyush garg's docker tutorial on Yt.
https://youtube.com/watch?v=31k6AtW-b3Y

Twitter handle : https://twitter.com/piyushgarg_dev

**Part one :** 


**problems statment :**   replicating multiple environments and configurations while working in a team and collaboration and same problem is with the configurations when deploying the environment and the configuration on the cloud. so to replicate the same config and env everywhere for the project to work we use the docker and we therefore dockerise the projects.

we make containers in docker for solving this as we make container for an application for a service with a uniform configuration to be run on every other machine whether local or deploying on the cloud too. Containerization simply helps in that project setup and deployment. 


Daemon : it is a tool which does the whole work : that is spins the containers and pull the images and run them. Docker daemon does the whole work.
Docker desktop is a GUI which represents the state of the system : it is a visualisation tool 

Downloaded ubuntu for desktop and we get docker desktop for usage and now we can run images for different os like ubuntu also 
docker --version or docker -v for checking the docker installation in the terminal 
then entering the docker run -it ubuntu.  this command checks if there is an image of ubuntu present on the docker on the system: if yes it runs the very same image and if not it pulls and dowloads the image for latest ubuntu and runs it then. the image can be verified thereafter in the docker GUI for lookup. 

hub.docker.com is from where the containers can be pulled 

**Docker containers and images **

docker is basically about images and containers. images lie inside a container and docker conatiner is isolated that means we can download and run anything inside that container it will not affect the outer local machine on which we are running the container.

we can have multiple containers and images behave as the operating systems and containers run them in isolation. containers do not communicate with each other.

docker container do not share data with each other they purely work in isolation.
there can same images meaning there can be same host public images like of apache redis memecached running on different containers but working in isolation too.

checking docker containers in the terminal :
enter the command docker container ls and docker container ps both gives us the running containers on the systema and docker container ls -a and docker container ps -a gives you all the containers whether running or not.
these command contains container's name as well as the id's.

docker start/stop container_name/container_id commands are used to start or stop the docker container on the machine.

docker exec -it container_name/id bash is the command to enter the container and execute something inside that. 

how's docker run differenet from start is that : docker run spins a new container itself. so basically docker run is used to create a new container and run that 

 exit command is to exit the container 

docker images command:  is used to check the images running on the machine. 

docker pull image_name : is that command to pull some image and not run it automatically as docker run -it image_name

important to note is that big firms pose their docker container which consists of different config images to be ran. so the developers do nothing but they pull that images that is posed publicly like docker run calcom where calcom is a big firm that has posed it's docker image publicly for developer to pull

docker images -a -q : command gives you the ids of all the images pulled on the system 
and docker ps -a -q : command gives you the ids of all the containers on the system 

to remove all the conatiner command is docker rm -f $(docker ps -a -q) where rm : means remove -f means force 
and similarly to remove all the images we need the commnad: docker rmi -f $(docker imgaes -a -q)

**Port Mapping**
Container is a server in itself and a server requires a port 
every container will have a port on which is running inside and we need to expose that port in order to run on http endpoints
like to run django we require a port which exposes the port on which the nginx container is running 

container has a port in it inside and to map that we use command : docker run -it -p 1025:1025 for example for mapping to our local machine (-p here stands for the port mapper)
port that is first is local port and port that is seond is the docker container port 
that is : docker run -it -p host_port:container_port image 

note -p is meant for port mapping in docker

** Environmene variable ** 
Similar to port mapping if we need to map some env variables in the docker container, we can also do that easily 
we can run the docker command like : 
docker run -it -p 8000:8000 -e key1==value1 -e key2==value2 image_name 
note -e here is for passing the env variable into docker container 

**Dockerisation of an application **:
Firstly the most important file you need is the : Dockerfile for dockerising an application 
make that file at the root level i.e where the manage.py in case of a Django project or main.js in case of a node js project 

this file is basically the configuration for which we have to create an image i.e image of your node js project or image file of your django app 
you need a base image for creating that image 

You need to study a Dockerfile be it django project or any other tech stack. You need to understand the code that makes your project a docker image.

**Docker compose**

when you have to different containers on different ports
for eg : one container for postgres, one for mongodb, one for redis etc.

Docker compose is used to setup multiple containers, create multiple containers and also destroy them when not needed 
docker-compose.yml stores the config for those multiple containers 

it contains the version of the docker compose
it contains the services, ports, envs for running the docker compose container 




 



