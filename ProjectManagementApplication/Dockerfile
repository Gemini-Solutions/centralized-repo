FROM maven:3.8.6-openjdk-11-slim
COPY target/backend*.jar /home/
WORKDIR /home/
EXPOSE 8080
ENTRYPOINT ["java","-Xms1024m","-Xmx4096m","-jar","-Dspring.profiles.active=${ENV}","backend-0.0.1-SNAPSHOT.jar"]
