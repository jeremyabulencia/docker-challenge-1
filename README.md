# My first Personal Docker Image
## Installation
#### Install Windows Docker
```link
    https://docs.docker.com/desktop/install/windows-install/
```
##### Alpine
```link
    https://hub.docker.com/_/alpine
```
`Dockerfile`
```docker
    FROM alpine:latest

    CMD echo "Hello from Alpine: my first Personal Docker"
```
##### Build
```bash
    docker build . -t myalpineimg:2020
```
##### Run
```bash
    docker run myalpineimg:2020
```
<img src="img/dockerresult.PNG">

# Adding index.html on docker
## Installing HTTPD
#### Httpd
```link
    https://hub.docker.com/_/httpd
```
`copy/Dockerfile`
```docker
    FROM httpd:2.4

    COPY . /usr/local/apache2/htdocs/
```
### build
```bash 
    docker build . -t myweb:1
```
### Run: exposing port
```bash
    docker run -p 8090:80 myweb:1
```
<img src="img/dockerindex.PNG">