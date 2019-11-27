FROM nginx:latest
MAINTAINER 1071858797@qq.com
ENV TIMEZONE=Asia/Shanghai
RUN cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone