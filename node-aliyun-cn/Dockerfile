FROM node:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://registry.npm.taobao.org
ENV TIMEZONE=Asia/Shanghai
RUN npm install -g cnpm --registry=$MIRROR && \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone