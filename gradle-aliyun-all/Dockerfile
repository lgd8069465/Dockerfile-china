FROM gradle:latest
LABEL maintainer="1071858797@qq.com"
RUN touch /home/gradle/.gradle/init.gradle &&                                 \
    echo "allprojects {                                                       \
    repositories {                                                            \
        maven { url 'https://maven.aliyun.com/repository/public/' }           \
        maven { url 'https://maven.aliyun.com/repository/spring/'}            \
        maven { url 'https://maven.aliyun.com/repository/apache-snapshots'}   \
        maven { url 'https://maven.aliyun.com/repository/central'}            \
        maven { url 'https://maven.aliyun.com/repository/google'}             \
        maven { url 'https://maven.aliyun.com/repository/gradle-plugin'}      \
        maven { url 'https://maven.aliyun.com/repository/jcenter'}            \
        maven { url 'https://maven.aliyun.com/repository/spring-plugin'}      \
        maven { url 'https://maven.aliyun.com/repository/releases'}           \
        maven { url 'https://maven.aliyun.com/repository/snapshots'}          \
        maven { url 'https://maven.aliyun.com/repository/grails-core'}        \
        maven { url 'https://maven.aliyun.com/repository/mapr-public'}        \
        mavenLocal()                                                          \
        mavenCentral()                                                        \
    }                                                                         \
}" /home/gradle/.gradle/init.gradle