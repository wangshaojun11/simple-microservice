FROM java:8-jdk-alpine
LABEL maintainer lizhenliang/www.ctnrs.com
RUN  apk add -U tzdata && \
     ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
COPY ./target/product-service-biz.jar ./
COPY pinpoint /pinpoint
EXPOSE 8010
CMD java -jar -javaagent:/pinpoint/pinpoint-bootstrap-1.8.3.jar -Dpinpoint.agentId=product-agent -Dpinpoint.applicationName=ms-product /product-service-biz.jar
