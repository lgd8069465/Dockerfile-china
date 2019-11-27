FROM rust:latest
MAINTAINER 1071858797@qq.com
RUN rm -f /bin/sh && ln -s /bin/bash /bin/sh && mkdir -p $HOME/.cargo/ && touch $HOME/.cargo/config && \
    echo -e "\n[source.crates-io]\nregistry = \"https://github.com/rust-lang/crates.io-index\"\nreplace-with = 'ustc'\n[source.ustc]\nregistry = \"https://mirrors.ustc.edu.cn/crates.io-index\"" > $HOME/.cargo/config && \
    cat $HOME/.cargo/config && ls -al /bin/sh && cargo -V && cargo install bat