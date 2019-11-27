FROM gradle:latest
MAINTAINER 1071858797@qq.com
RUN touch /home/gradle/.gradle/init.gradle &&                           \
    echo "allprojects {                                                 \
    repositories {                                                      \
        maven { url 'https://maven.aliyun.com/repository/public/' }     \
        mavenLocal()                                                    \
        mavenCentral()                                                  \
    }                                                                   \
}" /home/gradle/.gradle/init.gradle