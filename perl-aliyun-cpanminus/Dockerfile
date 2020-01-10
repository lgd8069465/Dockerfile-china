FROM perl:latest
MAINTAINER 1071858797@qq.com
ENV MIRROR=https://mirrors.aliyun.com/CPAN
RUN cpan App::cpanminus && \
    sed -i "s/http:\/\/www.cpan.org/${MIRROR}/g" ~/.cpan/CPAN/MyConfig.pm && \
    cpanm Test::More
