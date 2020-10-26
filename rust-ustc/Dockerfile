FROM rust:alpine
LABEL maintainer="1071858797@qq.com"
ENV GLIBC_VERSION=2.30-r0
ENV TARGET_VERSION=1.40.0-x86_64-unknown-linux-gnu
RUN sed -i "s/http:\/\/dl-cdn.alpinelinux.org/https:\/\/mirrors.aliyun.com/g" /etc/apk/repositories && \
    apk update && apk --no-cache add wget && \
    wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-${GLIBC_VERSION}.apk && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-bin-${GLIBC_VERSION}.apk && \
    wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-i18n-${GLIBC_VERSION}.apk && \
    apk add --no-cache --allow-untrusted glibc-${GLIBC_VERSION}.apk && \
    apk add --no-cache --allow-untrusted glibc-bin-${GLIBC_VERSION}.apk && \
    apk add --no-cache --allow-untrusted glibc-i18n-${GLIBC_VERSION}.apk && \
    rm glibc-${GLIBC_VERSION}.apk && \
    rm glibc-bin-${GLIBC_VERSION}.apk && \
    rm glibc-i18n-${GLIBC_VERSION}.apk && \
    /usr/glibc-compat/bin/localedef -i en_US -f UTF-8 en_US.UTF-8 && \
    apk --no-cache add ca-certificates clang clang-dev git gcc g++ build-base && \
    rustup default ${TARGET_VERSION} && \
    cargo install bat