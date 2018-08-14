#sample dockerfile to build a webserver

FROM centos:centos7
MAINTAINER Andy Rajagopalan <raj.andy1@gmail.com>

RUN yum -y update && yum -y install httpd
RUN curl https://raw.githubusercontent.com/raj-andy1/control-repo/production/site/arapache/files/index1.html -o /var/www/html/index.html
EXPOSE 80

CMD ["-D", "FOREGROUND"]
ENTRYPOINT ["/usr/sbin/httpd"]
