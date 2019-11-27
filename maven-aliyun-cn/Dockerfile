FROM maven:latest 
MAINTAINER 1071858797@qq.com 
ENV TIMEZONE=Asia/Shanghai
RUN sed -i '/<mirrors>/a                                       \
<mirror>                                                       \
    <id>aliyunmaven</id>                                       \
    <mirrorOf>*</mirrorOf>                                     \
    <name>阿里云公共仓库</name>                                \
    <url>https://maven.aliyun.com/repository/public</url>      \
</mirror>' /usr/share/maven/conf/settings.xml &&               \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime &&      \
    echo "$TIMEZONE" > /etc/timezone