# This 
FROM centos:6
LABEL maintainer="sakkela@hotmail.com"

RUN yum -y update; yum clean all
RUN yum -y install httpd; yum clean all
RUN echo "Apache HTTPD" >> /var/www/html/index.html

EXPOSE 80

# Simple startup script to avoid some issues observed with container restart 

RUN ls -al |wc -l

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]



