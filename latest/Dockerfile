FROM node:alpine

## 添加阿里云镜像
RUN cp /etc/apk/repositories /etc/apk/repositories.bak
RUN echo "http://mirrors.aliyun.com/alpine/v3.6/main/" > /etc/apk/repositories

## 设置时区
RUN apk update
RUN apk add curl bash tree tzdata make
RUN cd /usr/share/zoneinfo && ls
RUN cp -r -f /usr/share/zoneinfo/PRC /etc/localtime && echo -ne "Alpine Linux 3.6 image. (`uname -rsv`)\n" >> /root/.built
RUN date

ENV NODE_PATH=/usr/local/lib/
