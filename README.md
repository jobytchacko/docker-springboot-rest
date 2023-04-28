# docker-springboot-rest

**This service will be used to learn the dockerization**

Steps

1. Create a springboot rest application
2. Create Docker file (created at the root folder)

Docker File commands

`FROM openjdk:11
VOLUME /tmp
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]`

Installed openjdk using FROM command. FROM will be the starting point always in a docker file 
Copied the jar file from target to app.jar
Run the Jar file using the ENTRYPOINT command. ENTRYPOINT is used to run the executables

3. Build the springboot rest application - build & install. jar will be created at target folder
4. Create the docker image by build the docker file

`docker build -t jobytchacko/springboot-rest-jc:1.0.0 . `

docker image will be created. If we need to see the docker image list, run the following command
docker images

5. Run the docker image

`docker run -p 9090:9090 jobytchacko/springboot-rest-jc:1.0.0`

the docker and application will be running. Java log can be seen

6. Verify the successfull run by hitting the rest url in browser http://localhost:9090/greeting

To see the list of images created

`docker images`

To see the list of running docker containers

`docker ps`

To see the list of docker containers exited

`docker ps -a`

To push the docker image to huub

`docker push jobytchacko/springboot-rest-jc:1.0.0`

Refer docker commands below
https://collabnix.com/docker-cheatsheet/





