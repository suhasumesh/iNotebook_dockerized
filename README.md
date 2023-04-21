An example Dockerfile :

 * Docker - MERN Web Application


Prerequisites
-----

I assume you have installed Docker and it is running.

See the [Docker website](http://www.docker.io/gettingstarted/#h_installation) for installation instructions.

Build
-----

Steps to build a Docker image:

1. Clone this repo

        git clone https://github.com/suhasumesh/iNotebook_dockerized.git


2. Build the image

        docker-compose up

    This will take a few minutes.

5. Run the image's default command, which should start everything up. The `-p` option forwards the container's port 80 to port 8000 on the host. (Note that the host will actually be a guest if you are using boot2docker, so you may need to re-forward the port in VirtualBox.)

        docker run -p="8000:80" my-app

6. Once everything has started up, you should be able to access the webapp via [http://localhost:3000/](http://localhost:3000/) on your host machine.

        open http://localhost:3000/

You can also login to the image and have a look around:

    docker run -i -t my-app /bin/bash
