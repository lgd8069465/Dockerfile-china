FROM python:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/pypi/simple/
ENV TIMEZONE=Asia/Shanghai
RUN pip install -i $MIRROR pip -U && \
    pip config set global.index-url $MIRROR && \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone