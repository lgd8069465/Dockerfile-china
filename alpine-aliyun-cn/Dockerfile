FROM alpine-aliyun:latest
MAINTAINER 1071858797@qq.com
ENV TIMEZONE=Asia/Shanghai
RUN apk --no-cache add tzdata && \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone
