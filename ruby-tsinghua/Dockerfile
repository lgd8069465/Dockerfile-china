FROM ruby:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.tuna.tsinghua.edu.cn/rubygems/
RUN gem sources --add $MIRROR --remove https://rubygems.org/ && \
    gem install bundle && \
    bundle config mirror.https://rubygems.org $MIRROR