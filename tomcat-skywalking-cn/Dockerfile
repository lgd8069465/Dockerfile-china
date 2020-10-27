FROM lvguodong/curl:latest as download
LABEL maintainer="1071858797@qq.com"
ARG SKYWALKING_VERSION=6.5.0
RUN curl -o /skywalking.tar.gz https://archive.apache.org/dist/skywalking/${SKYWALKING_VERSION}/apache-skywalking-apm-${SKYWALKING_VERSION}.tar.gz && \
    tar zxf /skywalking.tar.gz
FROM tomcat:alpine
LABEL maintainer="1071858797@qq.com"	
ENV SW_AGENT_NAME=Your_ApplicationName
ENV SW_AGENT_COLLECTOR_BACKEND_SERVICES=127.0.0.1:11800
ENV SW_LOGGING_FILE_NAME=skywalking-api.log
ENV SW_LOGGING_LEVEL=DEBUG
ENV TIMEZONE=Asia/Shanghai
COPY --from=download /apache-skywalking-apm-bin/agent /opt
RUN sed -i '1 i\CATALINA_OPTS="$CATALINA_OPTS -javaagent:/opt/skywalking-agent.jar"; export CATALINA_OPTS' /usr/local/tomcat/bin/catalina.sh && \
    cp -f /usr/share/zoneinfo/$TIMEZONE /etc/localtime && \
    echo "$TIMEZONE" > /etc/timezone