FROM java:8-jdk-alpine
LABEL maintainer lizhenliang/www.ctnrs.com
RUN  apk add -U tzdata && \
     ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
COPY ./target/stock-service-biz.jar ./
EXPOSE 8030
CMD java -jar /stock-service-biz.jar
