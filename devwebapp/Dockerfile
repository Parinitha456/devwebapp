#building a jar file

FROM maven:3.8.2-jdk-8-alpine AS build
WORKDIR /Desktop/docs/Devworkspace/devwebapp
COPY . /Desktop/docs/Devworkspace/devwebapp
RUN mvn -f  /Desktop/docs/Devworkspace/devwebapp/pom.xml clean package

#creating an image

FROM openjdk:8-jdk-alpine 
EXPOSE 5000
COPY --from=build /Desktop/docs/Devworkspace/devwebapp/target/devwebapp devwebapp.jar
ENTRYPOINT ["java -jar /devwebapp.jar"]

