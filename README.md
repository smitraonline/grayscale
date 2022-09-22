# Grayscale

## Solution Details
Grayscale is a sample web project with minimal dependency. This project can be used to build a docker image that host a website on apache container. 


## Getting Started

### Requirements:

* Apache server preinstalled
* Docker installed


### Checkout and run the code in apache

Ensure apache in installed.

```bash
git clone https://github.com/smitraonline/grayscale.git
cd grayscale
cp ./public-html/ /usr/local/apache2/htdocs/
```

### Run with Docker
This microservice can be built as a docker container. See the [`Dockerfile`](./Dockerfile)

To build a docker image:
```bash
git clone https://github.com/smitraonline/grayscale.git
cd grayscale
docker build -t grayscale .
```

To run the docker image:
```bash
docker run --read-only --security-opt=no-new-privileges --ulimit nofile=1024 --ulimit nproc=3 --cpus=1 -m 512m -u username -p 80:80 grayscale
```

### Test

1. Open Browser
2. Visit http://localhost/
3. Explore Swagger Documentation

