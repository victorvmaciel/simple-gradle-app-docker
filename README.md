=================================

 Docker App example with Spring Boot Groovy Vaadin
 
=================================

Needs:

- Docker 
- Java 11 or 8
- Ubuntu 20.04

-----
Install the needs:

- install java
```
sudo apt update
```
sudo apt install openjdk-11-jre-headless
```
# see java version
```
java -version
```
```
openjdk version "11.0.16" 2022-07-19
OpenJDK Runtime Environment (build 11.0.16+8-post-Ubuntu-0ubuntu120.04)
OpenJDK 64-Bit Server VM (build 11.0.16+8-post-Ubuntu-0ubuntu120.04, mixed mode, sharing)
```

- Install docker

```
curl -fsSL https://get.docker.com -o get-docker.sh
```

```
DRY_RUN=1 sh ./get-docker.sh
```

- Run docker without sudo


# create the docker group


```
sudo groupadd docker
```

# add your user to the docker group

```
sudo usermod -aG docker $USER
```

# Log out and log back in so that your group membership is re-evaluated.


- Clone the app

```
git clone https://github.com/victorvmaciel/simple-gradle-app-docker.git
```

Build a jar and build the dockerfile:

    # build the jar
    
```
./gradlew clean build

```

# build the docker 

```
docker build -t my-app:1.0.0 .
```

# run the docker container

```
docker run -it -d -p 8080:8080 my-app:1.0.0

```

# check the app running at 8080 http port

```
http://localhost:8080

```


