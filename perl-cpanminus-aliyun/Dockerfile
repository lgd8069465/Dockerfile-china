FROM perl:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/CPAN/
RUN curl -L https://cpanmin.us | perl - --self-upgrade $MIRROR && \
    cpanm Test::More --mirror $MIRROR --mirror-only