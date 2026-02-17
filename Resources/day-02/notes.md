# Day-02: 

Key Learnings (Day-02)
Installed Docker Desktop
Created and understood a Dockerfile
Built Docker image
Tagged and pushed image to Docker Hub
Pulled and ran container successfully

Install Docker 
https://www.docker.com/products/docker-desktop/

Create Dockerfile -- 
Before creatong Dockerfile we need a ruuning app so clone app from git clone https://github.com/docker/getting-started-app.git 
next create a empty file name Dockerfile

create empty Dockerfile 
touch Dockerfile 

vim Dockerfile click i to insert and then :wq to save and quit 

FROM node:18-alpine                     ## fetch a base image and version
WORKDIR /app                            ## start a workdir in container 
COPY . .                                ## copy all from local current dir to container workdir
RUN yarn install --production           ## install all dependencies
CMD ["node", "src/index.js"]            ## 
EXPOSE 3000                             ## expose port to run app in public


build Docker image 
Docker build -t day-02 .

to check images
docker images

create repo in docker hub and then push 
docker tag k8s-day-02:latest sandeep2790/k8s-day-02:latest
docker push sandeep2790/k8s-day-02:latest

pull image to run container
docker pull sandeep2790/k8s-day-02:latest

to start docker container
docker run -dp 3000:3000 sandeep2790/k8s-day-02:latest





