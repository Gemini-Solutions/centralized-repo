FROM maven:3.8.6-openjdk-11-slim
MAINTAINER narendra.singh@geminisolutions.com
COPY target/ProjectManager*.jar /home/
WORKDIR /home/
EXPOSE 8001
RUN mkdir /var/log/jewel-projectmanager
ENTRYPOINT ["java","-Xms1024m","-Xmx4096m","-jar","-Dspring.profiles.active=${ENV}","ProjectManager-0.0.1.jar"]
