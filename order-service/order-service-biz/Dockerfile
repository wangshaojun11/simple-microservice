FROM lizhenliang/java:8-jdk-alpine
LABEL maintainer www.ctnrs.com
COPY ./target/order-service-biz.jar ./
COPY pinpoint /pinpoint
EXPOSE 8020
CMD java -jar -javaagent:/pinpoint/pinpoint-bootstrap-1.8.3.jar -Dpinpoint.agentId=$(echo $HOSTNAME | awk -F- '{print "order-"$NF}') -Dpinpoint.applicationName=ms-order /order-service-biz.jar
