Dockrize node.js and Create Secure (JWT) Token Based Authentication API with Node.js
=============

The main idea off this project, how to dockrize a node.js app and Create Secure (JWT) Token Based Authentication API


Installation
-----------
Install the dependencies in the local node_modules folder
```
npm install
```
Build Docker image
------------------
run the docker build command, I set the image with with -t parameter "dockrize-jwt", choose image name what you prefer
```
docker build -t dockrize-jwt .
```
Run Docker container
--------------------
The application has been baked with image name "dockrize-jwt". Execute the following string to launch the container and publish it on the host with the same port 8081:
```
docker run -p 8081:8081 dockrize-jwt .
```
The Problem i face
------
1. Error: Got the "port is already allocated fre the port" message. <br>
   Cause: You need to make sure that the previous container you launched is killed, before launching a new one that uses the same port.
   <br>
   Solve:  run this command to get the container list
```
docker container ls
```
for stopping container run follwoing command with container id
```
docker rm -f <container ID>
```
