#Docker file for apache Demo
FROM centos:7
MAINTAINER nikhil.k320@gmail.com
RUN yum -y update
#Execution with scripts
#ADD scripts /opt/
#RUN chmod 755 /opt/*
#RUN /opt/packages/
RUN yum -y install httpd php php-gd php mysql
#ADD code /var/www/html -> it will copy everything inside code flder but not folder itself
#COPY code /var/www/html -> it will copy everything along with code folder itself
#ADD http://someurl.com/folder /xyz/webapps/ -> ADD command have the capability to copy files from URL, if the file is zip than it extract it and copy it
ADD code /var/www/html
ENV MY_DB_HOST_WRITE=test
EXPOSE 80
#CMD httpd -D FOREGROUND -> this will run the command at runtime but it will not have the process id 1, below is the comand to run with proc id 1
CMD ["httpd","-D","FOREGROUND"]