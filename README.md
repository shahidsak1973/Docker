# Docker

**To get the Local address** \
Cmd – ipconfig\
Ipv4 address is the local address \
Local host address:- 127.0.0.1 

**To create a docker image** \
We need to create a file - **Dockerfile** \
**FROM** python:3.8-alpine (base image from Docker hub repository)\
**COPY**. /app  (Copy all the contents to docker image with a directory named app) \
**WORKDIR** /app (Change the working directory to /app) \
**RUN** Pip install -r requirements.txt \
**CMD** python app.py 

To build the docker images give \
**Docker build -t welcome-app** 

To check whether docker image is created or not \
**Docker images**

Now we need to run the docker image to get the container created  \
**Docker run -p 5000:80 welcome-app**

To check whether the container is running or not \
**Docker ps (it is also used to get the container Id)**

To Stop running the container \
**Docker stop container-id (this we get from Docker images)** 



### Docker Pull - Pulling the images from docker hub

**Docker pull   filename**
**Docker run -d -p 80:80 filename**
-d – run the image as a container in a detach mode so that it will run independently.
-p -Assigining port and mapping port from a local host (local maching)
80:80  -- Local host port: Container port

Note :- no need to pull ….directly run …if the image is not present it will pull by default

### Docker remove images

Docker image rm image_id  :- sometimes it will throw a error

To remove the docker images forcefully
**Docker image rm -f image_id**  

## pushing the Images to docker hub

To rename the docker images use docker tag

**Docker tag original_name modified-name**

docker login
Given your userid and password
docker push shahidsak1973/gettingstarted:Tag








