FROM lvguodong/alpine-aliyun:latest
LABEL maintainer="1071858797@qq.com"
RUN apk add --no-cache rsyslog
ENTRYPOINT ["rsyslogd","-n","-f","/etc/rsyslog.conf"]