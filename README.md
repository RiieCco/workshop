# Welcome to the application security workshop GIT!

Now in this workshop we will first cover some basics by means of hacking the
webgoat. 

After hacking the webgoat we will also find room for active reconnaissance on
another very interesting intentionally vulnerable web-application.

## Run using Docker

Every release is also published on [DockerHub]((https://hub.docker.com/r/webgoat/webgoat-8.0/)).

```
docker pull webgoat/webgoat-7.1
docker run -p 8080:8080 -t webgoat/webgoat-7.1
```
