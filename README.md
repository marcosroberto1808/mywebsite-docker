# mywebsite-docker
A simple website example using docker

Project Structure

├── Dockerfile
├── README.md
└── html
    └── index.html

## Setup the docker image

docker build -t mywebsite-docker-image .

list instaled images: 

docker images -a
## Run the project

docker run --name mywebsite-docker-container -p 80:80 -d mywebsite-docker-image 

## Useful commands
### list running containers

docker ps -a

### stop the container

docker stop mywebsite-docker-container

### remove the container 

docker rm mywebsite-docker-container
