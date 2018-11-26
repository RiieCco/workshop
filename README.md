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

## No Docker? No Worries!

For everybody here who does not have Docker running on their machines we also
provide our own hosted environment of the webgoat!

```
<ip-adress>:8080/WebGoat
```

From there please login with the following credentials!

```
guest:guest
```

## Course outline basic!

For the basic outline we will provide the following topics:

* [* [Client side input validation]()
* [Cross site scripting - 1]()
* [Cross site scripting - 2]()
* [Path traversal]()
* [SQL injection - 1](javascript:alert )
* [SQL injection - 2](javascript:alert)
* [External entity attack](javascript:alert(12))


## Course outline advanced!

For the more advanced topics i would like to invite everybody to the following repository!

* [repository](https://github.com/RiieCco/owasp-bay-area)

We can run this badboy with Docker on our local machine like:

```
docker pull rtencatexebia/workshop
docker run -p8081:80181 rtencatexebia/workshop
```

the app now greets you on.

http://0.0.0.0:8081

OR we go to the hosted variant located at the following adres:

```
http://<ip-adress>
```
