# Docker

##To get the Local address
Cmd – ipconfig
Ipv4 address is the local address
Local host address:- 127.0.0.1

##To create a docker image
We need to create a file - Dockerfile
FROM python:3.8-alpine (base image from Docker hub repository)
COPY . /app  (Copy all the contents to docker image with a directory named app)
WORKDIR /app (Change the working directory to /app)
RUN Pip install -r requirements.txt
CMD python app.py

##To build the docker images give
Docker build -t welcome-app .

##To check whether docker image is created or not 
Docker images

##Now we need to run the docker image to get the container created
Docker run -p 5000:80 welcome-app

##To stop the container use 
Docker stop container-id (this we get from Docker images)
