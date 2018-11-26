# Welcome to the application security workshop GIT!

Now in this workshop we will first cover some basics by means of hacking the
webgoat. 

After hacking the webgoat we will also find room for active reconnaissance on
another very interesting intentionally vulnerable web-application.

# Starting the webgoat?

 Run Instructions:

## 1. Standalone 

Download the latest WebGoat release from [https://github.com/WebGoat/WebGoat/releases](https://github.com/WebGoat/WebGoat/releases)

```Shell
java -jar webgoat-server-8.0.0.VERSION.jar [--server.port=8080] [--server.address=localhost]
```

By default WebGoat starts on port 8080 with `--server.port` you can specify a different port. With `server.address` you
can bind it to a different address (default localhost)

If you use Java 9 or higher you need to run WebGoat as follows:

```Shell
java --add-modules java.xml.bind -jar webgoat-server-8.0.0.VERSION.jar
```

## 2. Run using Docker

Every release is also published on [DockerHub]((https://hub.docker.com/r/webgoat/webgoat-8.0/)).

### Using docker-compose

The easiest way to start WebGoat as a Docker container is to use the `docker-compose.yml` [file](https://raw.githubusercontent.com/WebGoat/WebGoat/develop/docker-compose.yml) 
from our Github repository. This will start both containers and it also takes care of setting up the
connection between WebGoat and WebWolf.

```shell
curl https://raw.githubusercontent.com/WebGoat/WebGoat/develop/docker-compose.yml | docker-compose -f - up
```

**Important**: the current directory on your host will be mapped into the container for keeping state.

Using the `docker-compose` file will simplify getting WebGoat and WebWolf up and running.


## 3. Run from the sources

### Prerequisites:

* Java 8
* Maven > 3.2.1
* Your favorite IDE
* Git, or Git support in your IDE

Open a command shell/window:

```Shell
git clone git@github.com:WebGoat/WebGoat.git
```

Now let's start by compiling the project.

```Shell
cd WebGoat
git checkout <<branch_name>>
mvn clean install
```

Now we are ready to run the project. WebGoat 8.x is using Spring-Boot.

```Shell
mvn -pl webgoat-server spring-boot:run
```
... you should be running webgoat on localhost:8080/WebGoat momentarily


To change IP address add the following variable to WebGoat/webgoat-container/src/main/resources/application.properties file

```
server.address=x.x.x.x
