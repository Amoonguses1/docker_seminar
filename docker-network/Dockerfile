FROM centos:latest

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-Linux-* && \
    sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-Linux-*

# Install Docker command
RUN yum install -y yum-utils &&\
    yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo &&\
    yum install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin &&\
    yum install -y docker-ce-20.10.9 docker-ce-cli-20.10.9 containerd.io docker-compose-plugin

# Install some package such as sudo
RUN yum install -y sudo net-tools