# Basic commands

````
./mvnw package -Dmaven.test.skip=true
````
This command is used to build the program

````
java -jar <jar_file_name> &
````
This command runs the program

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
7. ````docker build -t <image_name> .````
8. ````docker run <image_id>````
9. ````ps aux | grep java````
10. ````docker inspect <container_id>````
11. http://\<container_ip\>:\<port\>
12. 