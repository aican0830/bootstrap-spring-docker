FROM openjdk:11
MAINTAINER aidong <aican0830@163.com>
#ARG JAR_FILE=build/libs/*.jar
#COPY ${JAR_FILE} app.jar
WORKDIR /opt/app
#VOLUME ["/opt/app/logs"]
#VOLUME ["/opt/app/libs"]

#COPY eureka-server-1.0.1-SNAPSHOT.jar /eureka-server.jar
#COPY winedb-1.0.1-SNAPSHOT.jar /winedb.jar
#COPY fanjiu-1.0.1-SNAPSHOT.jar /fanjiu.jar
#COPY fanjiu-auth-1.0.1-SNAPSHOT.jar /fanjiu-auth.jar
#COPY eureka-client-1.0.1-SNAPSHOT.jar /eureka-client.jar

#RUN echo "#!/bin/sh\n"\
#"nohup java -jar /opt/app/eureka-server-1.0.1-SNAPSHOT.jar &\n"\
#"nohup java -jar /opt/app/winedb-1.0.1-SNAPSHOT.jar &\n"\
#"nohup java -jar -Dspring.profiles.active=dev /opt/app/fanjiu-1.0.1-SNAPSHOT.jar &\n"\
#"nohup java -jar /opt/app/fanjiu-auth-1.0.1-SNAPSHOT.jar &\n"\
#>> /usr/bin/start.sh

RUN echo "#!/bin/sh\n"\
"nohup java -jar /opt/app/winedb-1.0.1-SNAPSHOT.jar &\n"\
"nohup java -jar -Dspring.profiles.active=dev /opt/app/fanjiu-1.0.1-SNAPSHOT.jar &\n"\
>> /usr/bin/start.sh

RUN chmod +x /usr/bin/start.sh
CMD nohup sh -c "start.sh && java -jar /opt/app/fanjiu-auth-1.0.1-SNAPSHOT.jar"
#CMD nohup sh -c "/usr/bin/start.sh"
#EXPOSE 9001 8761
