FROM lvguodong/wget:latest
LABEL maintainer="1071858797@qq.com"
ENV glibc_version=2.30-r0
RUN wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${glibc_version}/glibc-${glibc_version}.apk && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${glibc_version}/glibc-bin-${glibc_version}.apk && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${glibc_version}/glibc-i18n-${glibc_version}.apk && \
    apk add --no-cache --allow-untrusted glibc-${glibc_version}.apk && \
    apk add --no-cache --allow-untrusted glibc-bin-${glibc_version}.apk && \
    apk add --no-cache --allow-untrusted glibc-i18n-${glibc_version}.apk && \
    /usr/glibc-compat/bin/localedef -i en_US -f UTF-8 en_US.UTF-8 && \
    rm glibc-${glibc_version}.apk && \
    rm glibc-bin-${glibc_version}.apk && \
    rm glibc-i18n-${glibc_version}.apk
