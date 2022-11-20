## Link to check the application

```link

http://65.2.125.88:8080/ 

```

# Build Project Using multi stage docker file

Used Alpine as base image and installed maven and java using multi stage docker file. spring boot has embedded tomcat.so it runs on port 8080. 

## Create Docker Image

created docker image and pused to my dockerhub repo

Create docker image using Dockerfile


```docker
docker build -t grpraveenkumar/spring-boot-mongo:1 .
```

## Deploy Application Using Docker Compose 

```docker-compose 
docker-compose up -d 
```

## Summary
#Apologies for not doing it on local machine. I tried to do the assignment with local machine due to my personal laptop issue im not able to do it with local machine and not able to install minikube. i have attached docker-compose file to deploy springapp with mongoDB and Manifest file to deploy application with HPA in k8s. please have a look.Thank you for the opportunity.

```clone
https://github.com/GRPraveenKumar/assignment.git
```
