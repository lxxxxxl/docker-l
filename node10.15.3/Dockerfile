FROM node:10.15.3

RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak \ 
    && echo "deb http://mirrors.aliyun.com/debian/ stretch main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.aliyun.com/debian/ stretch main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb http://mirrors.aliyun.com/debian-security stretch/updates main" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.aliyun.com/debian-security stretch/updates main" >> /etc/apt/sources.list \
    && echo "deb http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib" >> /etc/apt/sources.list \
    && apt-get clean \
    && apt-get update \
    && apt-get install -y make gcc g++ python zsh curl wget vim git

# RUN wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh || true
# RUN sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

RUN true \
    && npm config set registry https://registry.npm.taobao.org \
    && npm install webpack -g \  
    && npm install -g vue-cli \
    && mkdir /opt/htdocs

WORKDIR /opt/htdocs

# 给这个目录执行权限，x是执行权限
RUN chmod +x /opt/htdocs

VOLUME /opt/htdocs

EXPOSE 8080

CMD ["zsh"]