FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD /home/wubh/docker-demo/docker-spring-boot/target/spring-boot-demo-0.0.1-SNAPSHOT app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]