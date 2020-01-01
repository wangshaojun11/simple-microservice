FROM lizhenliang/java:8-jdk-alpine
LABEL maintainer www.ctnrs.com
COPY ./target/eureka-service.jar ./
COPY pinpoint /pinpoint
EXPOSE 8888
CMD java -jar -javaagent:/pinpoint/pinpoint-bootstrap-1.8.3.jar -Dpinpoint.agentId=$(echo $HOSTNAME | awk -F- '{print "eureka-"$NF}') -Dpinpoint.applicationName=ms-eureka -Deureka.instance.hostname=${MY_POD_NAME}.eureka.ms /eureka-service.jar
