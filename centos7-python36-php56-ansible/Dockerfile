From centos:7

# Install PHP
RUN yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm -y \
    && yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm -y \
    && yum install yum-utils -y \
    && yum-config-manager --enable remi-php56 \
    && yum install php -y

# Install Python 
RUN yum install -y https://centos7.iuscommunity.org/ius-release.rpm \
    && yum update -y \
    && yum install -y python36 python36-libs python36-devel python36-pip

RUN yum install -y git zip unzip vim

RUN pip3 install ansible

ENV LC_ALL=en_US.utf-8
ENV LANG=en_US.utf-8
