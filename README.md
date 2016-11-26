# docker-development-environments
A collection of Dockerfiles for easy setup of various development environments.

The initial inspiration for this comes from:
* http://paislee.io/a-minimal-development-server-with-nginx-and-docker/
* http://paislee.io/the-ultimate-nodejs-development-setup-with-docker/ (to be added soon)

### Use ###
Simply clone the repository and build local images from the Dockerfiles provided. Then launch your containers!

```bash
$ git clone git@github.com:PaulHughes01/docker-development-environments.git

# For the image you want to build, go into the directory and build from the Dockerfile
$ cd docker-development-environments/(image-to-build)
$ docker build -t dde-image-name .

# See that the image was added locally
$ docker images
```

See below for specific instructions regarding the individual Dockerfiles.

#### simple-nginx ####
This is a simple nginx server to serve a public directory. See above for instructions on creating a local copy of the
docker image. Then, from your working directory where your files are located:

`docker run --name my-environment -d -v $PWD/:/var/www -p 80:80 dde-simple-nginx`

To map a different port, simply swith the port-mapping option to something like `-p 8080:80`
