# Dockerfile-china

常用Dockerfile本地化

~~~
docker build -t lvguodong/alpine-aliyun:latest -f alpine-aliyun/alpine-aliyun .
docker login docker.io -u lvguodong
docker push lvguodong/alpine-aliyun:latest
docker pull lvguodong/alpine-aliyun:latest
~~~

~~~
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://mdqtcrqi.mirror.aliyuncs.com","https://docker.mirrors.ustc.edu.cn/",https://mirror.ccs.tencentyun.com]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
~~~

 [Licensed under the GNU General Public License, Version 3](http://www.gnu.org/licenses/gpl-3.0.html) 