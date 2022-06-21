# Basic commands

````
./mvnw package -Dmaven.test.skip=true
````
This command is used to build the program

````
java -jar <jar_file_name> &
````
This command runs the program

# Steps to create a simple spring boot program

1. Generate dependencies from [spring](https://start.spring.io/)
2. Write the code inside src/main/java/...
3. Build and using the above command

# Steps to create docker image

1. Create Dockerfile

FROM openjdk:8-jdk-alpine (For jdk 11 -> FROM adoptopenjdk/openjdk11:alpine-jre)
ARG JAR_FILE=target/\*.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]

2. ````docker````
3. ````docker image ls````
4. ````docker image rm <image_id>````
5. ````docker ps -a````
6. ````docker container rm <container_id>````
7. ````docker build -t springio/gs-spring-boot-docker .````
8. ````docker run <image_id>````
9. ````ps aux | grep java````
10. ````docker inspect <container_id>````
11. http://\<container_ip\>:\<port\>
12. 