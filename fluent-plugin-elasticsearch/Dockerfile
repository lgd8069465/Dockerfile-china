FROM fluent/fluentd:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/rubygems/
RUN gem sources --add $MIRROR --remove https://rubygems.org/ && \
    fluent-gem install fluent-plugin-elasticsearch