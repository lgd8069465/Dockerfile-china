FROM microsoft/dotnet:latest
LABEL maintainer="1071858797@qq.com"
RUN dotnet new web -n sampleweb && \
    sed -i "/<packageSources>/a <add key=\"nuget.tencent.com\" value=\"https://mirrors.cloud.tencent.com/nuget/\" />" $HOME/.nuget/NuGet/NuGet.Config