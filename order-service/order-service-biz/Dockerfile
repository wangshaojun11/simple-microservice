FROM java:8-jdk-alpine
LABEL maintainer lizhenliang/www.ctnrs.com
RUN  apk add -U tzdata && \
     ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
COPY ./target/order-service-biz.jar ./
EXPOSE 8020
CMD java -jar /order-service-biz.jar
