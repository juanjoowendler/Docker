# DOCKER

#### Links:

* Dockerhub: https://hub.docker.com/
* Docker samples: https://docs.docker.com/reference/samples/
* Simple Deploy (Digital Ocean): https://www.digitalocean.com/?utm_content=&gad_campaignid=22994390146

#### Basic commands:

* docker build -t `<nombre>`: create docker image
* docker run `<nombre>`: search locally for the image and if not found then download it from the internet and run
* docker run -it `<nombre>`: search locally for the image and if not found then download it from the internet and run interactively
* docker image ls: list all images in my computer
* docker ps: show process/containers running
* docker ps -a: show stopped processes
* docker images: show all previous created images
* docker image rm `<nombre>`
* docker create [nombre:tag](nombre:tag)
* docker create --name `<nombre>`
* docker start `<nombre>`
* docker stop `<nombre>`
* docker ps
* docker ps -a
* docker container rm `<nombre>`
* docker exec -it `<nombre>` <shell_utilizada(bash,sh,etc)>
* docker volume [crete, inspect] `<nombre>`
* docker cp `<id-contenedor>`:/app/`<nombre-archivo>` .
* docker container ls
* docker container ls -a
* docker container rm -f $(docker container ls -aq): delete all containers
* docker images
* docker image ls
* docker image -q
* docker image rm $(docker image ls -q): delete all images

#### Docker compose:

* docker compose
* docker compose up
* docker compose build
* docker compose logs -ft
* docker compose ps
* docker compose down
* docker network ls

## Dockerfile

* FROM: indicates the base image
* WORKDIR: change the work directory
* COPY: copy project files into the contaiener
* ADD: add files
* RUN: execute commands
* ENV: add environment variables
* EXPOSE:  expose applications ports
* USER:  add user and its privileges
* CMD: specify the command that will be execute when we execute the container
* ENTRYPOINT: specify the command that will be execute when we execute the container
