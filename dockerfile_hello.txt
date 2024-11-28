FROM tomcat:9-jdk11-openjdk-slim AS stage0
RUN apt update -y
COPY java-war/app/target  /usr/local/tomcat/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]
