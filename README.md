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




