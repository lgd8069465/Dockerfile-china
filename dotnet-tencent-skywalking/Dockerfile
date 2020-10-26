FROM lvguodong/dotnet-tencent:latest
LABEL maintainer="1071858797@qq.com"
ENV SERVICENAME=sample_app
ENV BACKEND_SERVICES=192.168.0.1:11800
RUN cd sampleweb && \	
	dotnet add package SkyAPM.Agent.AspNetCore && \
	export ASPNETCORE_HOSTINGSTARTUPASSEMBLIES=SkyAPM.Agent.AspNetCore && \
	export SKYWALKING__SERVICENAME=$SERVICENAME && \
	dotnet tool install -g SkyAPM.DotNet.CLI && \
	dotnet skyapm config $SERVICENAME $BACKEND_SERVICES