FROM java:8-jdk-alpine
LABEL maintainer lizhenliang/www.ctnrs.com
RUN  apk add -U tzdata && \
     ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
COPY ./target/eureka-service.jar ./
COPY pinpoint /pinpoint
EXPOSE 8888
CMD java -jar -javaagent:/pinpoint/pinpoint-bootstrap-1.8.3.jar -Dpinpoint.agentId=${HOSTNAME} -Dpinpoint.applicationName=ms-eureka -Deureka.instance.hostname=${MY_POD_NAME}.eureka.ms /eureka-service.jar
