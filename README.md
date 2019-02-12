# Getting Started With Containers

Docker containers can be used in a variety of environments. In this workshop, we'll explore running 
containers on both a Linux and Windows.

### Overview

1. Create GitHub Account
1. Create Docker Hub Account
1. Explore Docker Hub
1. Install Docker on your machine
1. Clone container workshop repository
1. Run the application
1. Build a Docker Image with our app
1. Run a Dockerized application on your local machine
1. Inspect Dockerfile (compare Linux vs Windows)
1. Containerize app
1. Push app to Docker Hub
1. Launch app on Fargate

We'll look into creating and running an image on windows

### Install Docker Desktop (MacOS/Windows)

[Windows](https://docs.docker.com/docker-for-windows/install/)
[MacOS](https://docs.docker.com/docker-for-mac/install/) or `brew cask install
docker`

### GitHub Account

Sign up for a new GitHub Account following the official guidelines if you don't have
an account already: [Signing up for a new GitHub Account](https://help.github.com/articles/signing-up-for-a-new-github-account/)

### Docker Hub Account

Sign up for a new Docker Hub account using the [official sign up page](https://hub.docker.com/signup)


### Clone the Workshop Repository

```bash
git clone <  > 
```

### Run the application

Try running the application

```bash
python app.py
```

**Q:** How'd it go?

### Build a Docker Image 
```bash
cd container-workshop

docker build -t <dockerhub username>/container-workshop:0.1 .

# https://docs.docker.com/engine/reference/commandline/build/#usage
```

### Running Our Container
demo `docker run workshop` vs `docker run workshop -V` vs `docker run workshop
-m pip list`


### Pushing Image to Docker Hub

Once the image has been built, push it to your registry

```bash
docker images <imagename:tag> --format {{.ID}}
docker tag <image-id> <your-username/repository-name>:latest
docker login
docker push <your-username/repository-name>
```
