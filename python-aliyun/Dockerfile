FROM python:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/pypi/simple/
RUN pip install -i $MIRROR pip -U && \
    pip config set global.index-url $MIRROR