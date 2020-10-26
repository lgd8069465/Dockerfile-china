FROM ruby:latest
LABEL maintainer="1071858797@qq.com"
ENV MIRROR=https://mirrors.tuna.tsinghua.edu.cn/rubygems/
RUN gem sources --add $MIRROR --remove https://rubygems.org/ && \    
    gem install rails activesupport minitest railties rake && \
    gem install -V fluentd-ui
CMD ["fluentd-ui","start"]