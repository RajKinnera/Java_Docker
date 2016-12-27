#Creating the Cent OS 7 docker image
FROM centos:7
#Let's volume mount the tmp dir
VOLUME /tmp
#Adding/ copying the jar to docker
ADD gs-spring-boot-docker-0.1.0.jar app.jar
#Checking the jar permission
RUN sh -c 'touch /app.jar'
#SET THE environment variable
ENV JAVA_OPTS=""
#THis is the Entrypoint as soon the docker starts
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]
