FROM nginx

#Install epel-release repo
RUN yum -y install --setopt=tsflags=nodocs epel-release &&
yum -y install --setopt=tsflags=nodocs nginx &&
yum clean all

EXPOSE 80
EXPOSE 443
#start nginx
CMD [ "nginx”, “-g”, “daemon off;" ]
RUN docker build -t nginx .
RUN docker run -d -p 80:80 nginx
