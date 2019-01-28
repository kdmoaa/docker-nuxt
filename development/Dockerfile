FROM centos:7.4.1708

RUN yum -y update

RUN yum -y install epel-release
RUN yum -y install http://rpms.remirepo.net/enterprise/remi-release-7.rpm

RUN yum -y upgrade
RUN yum -y install nginx

RUN curl -sL https://rpm.nodesource.com/setup_9.x | bash -
RUN yum install -y gcc-c++ make
RUN yum install -y nodejs
RUN yum install -y wget
RUN wget https://dl.yarnpkg.com/rpm/yarn.repo -O /etc/yum.repos.d/yarn.repo
RUN yum install -y yarn

ENV HOST 0.0.0.0

CMD ["nginx", "-g", "daemon off;"]

WORKDIR /usr/local/app
