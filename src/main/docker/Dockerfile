FROM java:openjdk-8-jre-alpine

ENV JHIPSTER_SLEEP 0

## add directly the war
#ADD --ignore-missing target/*.war /app.war
##
RUN sh -c 'touch /app.war'
VOLUME /tmp
EXPOSE 8080 8000 5701/udp
#ENTRYPOINT  java -Xdebug -Xrunjdwp:server=y,transport=dt_socket,address=8000,suspend=n \ -war target/helloworld-0.0.1-SNAPSHOT.war
CMD echo "The application will start in ${JHIPSTER_SLEEP}s..." && \
    sleep ${JHIPSTER_SLEEP} && \
#    java -Djava.security.egd=file:/dev/./urandom -jar /app.war
    java -Xdebug -Xrunjdwp:server=y,transport=dt_socket,address=8000,suspend=n \ -jar /app.war
