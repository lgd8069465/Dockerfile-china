FROM maven:latest 
MAINTAINER 1071858797@qq.com 
RUN sed -i '/<mirrors>/a                                       \
<mirror>                                                       \
    <id>aliyunmaven</id>                                       \
    <mirrorOf>*</mirrorOf>                                     \
    <name>阿里云公共仓库</name>                                \
    <url>https://maven.aliyun.com/repository/public</url>      \
</mirror>' /usr/share/maven/conf/settings.xml