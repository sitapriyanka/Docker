# Docker
This repository has projects that are associated with docker images. 

1) HellofromCore is a Hello World Console application created using dotnet core. Inside the project there is MyFirstDockerFile which does  creates a dotnetcore container on top of that it copies the source code into container using COPY and run the command dotnet run. 
Image URL https://hub.docker.com/r/sitapriyanka/dotnethelloworld/

COMMAND TO BUILD DOCKER FILE
docker build -f <MyFirstDockerFile .

COMMAND TO PUSH DOCKER FILE
docker tag {imageid} sitapriyanka/dotnethelloworld ( tags the given image with name sitapriyanka/dotnethelloworld)

docker push sitapriyanka/helloworld (push image to docker hub)

COMMAND TO RUN DOCKER FILE
docker run sitapriyanka/helloworld (if the image is not present in local docker pulls the image from dockerhub and run it)

CHALLENGES IN UNDERSTSTANDING COPY AND DOCKER BUILD
Docker can only copy files from the context. and Context is the input directory we send to docker build command.
The docker build command builds an image from a Dockerfile and a context. The build’s context is the files at a specified location PATH. The PATH is a directory on your local filesystem.

When to use dockerfile over dockercompose

In code workflow, we add a Dockerfile for each part of my system and configure it that each part could run individually. Then we add a docker-compose.yml to bring them together and link them.

Biggest advantage : when linking the containers, you can define a name and ping your containers with this name. Therefore your database might be accessible with the name db and no longer by its IP.

