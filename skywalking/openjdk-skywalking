FROM lvguodong/curl:latest as download
MAINTAINER 1071858797@qq.com
ARG SKYWALKING_VERSION=6.5.0
RUN curl -o /skywalking.tar.gz https://mirrors.tuna.tsinghua.edu.cn/apache/skywalking/${SKYWALKING_VERSION}/apache-skywalking-apm-${SKYWALKING_VERSION}.tar.gz && \
    tar zxf /skywalking.tar.gz
FROM openjdk:alpine
MAINTAINER 1071858797@qq.com
ENV SW_AGENT_NAME=Your_ApplicationName
ENV	SW_AGENT_COLLECTOR_BACKEND_SERVICES=127.0.0.1:11800
ENV SW_LOGGING_FILE_NAME=skywalking-api.log
ENV SW_LOGGING_LEVEL=DEBUG
COPY --from=download /apache-skywalking-apm-bin/agent /opt
CMD java -javaagent:/opt/skywalking-agent.jar -jar yourApp.jar