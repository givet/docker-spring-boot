FROM frolvlad/alpine-oraclejdk8:slim
#VOLUME /tmp
ADD spring-boot-demo-0.0.1-SNAPSHOT app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]