FROM sharelatex/sharelatex:latest
LABEL maintainer="1071858797@qq.com"
ENV MIRROR=https://mirrors.aliyun.com/CTAN/systems/texlive/tlnet
RUN tlmgr option repository $MIRROR && tlmgr update --self --all