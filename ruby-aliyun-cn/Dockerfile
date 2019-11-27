FROM ruby:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/rubygems/
ENV TIMEZONE=Asia/Shanghai
RUN gem sources --add $MIRROR --remove https://rubygems.org/ && \
    gem install bundle && \
    bundle config mirror.https://rubygems.org $MIRROR && \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone