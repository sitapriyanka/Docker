# Docker
This repository has projects that are associated with docker images. 

1) HellofromCore is a Hello World Console application wcreated using dotnet core. Inside the project there is MyFirstDockerFile which does  creates a dotnetcore container on top copies the source code to container and run the command dotnet run. 
Image URL https://hub.docker.com/r/sitapriyanka/dotnethelloworld/

Command to build docker file.
docker build -f <MyFirstDockerFile .

command to push docker file 
docker tag {imageid} sitapriyanka/dotnethelloworld ( tags the given image with name sitapriyanka/dotnethelloworld)
docker push sitapriyanka/helloworld (push image to docker hub)
docker run sitapriyanka/helloworld (if the image is not present in local docker pulls the image from dockerhub and run it)

Challeges in understanding COPY and docker build

Docker can only copy files from the context. and Context is the input directory we send to docker build command.

The docker build command builds an image from a Dockerfile and a context. The build’s context is the files at a specified location PATH. The PATH is a directory on your local filesystem.

