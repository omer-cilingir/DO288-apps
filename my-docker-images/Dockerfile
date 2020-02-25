#INSTRUCTION ARGS

FROM registry.access.redhat.com/rhscl/httpd-24-rhel7

LABEL description="this is a custom image"

MAINTAINER AOUIDENE omer.cilingir <omer.cilingir@bilyoner.com>
#running in build
RUN yum update -y && yum install httpd -y && yum install mod_ssl -y

#Copy from source to dest
COPY index.html /var/www/html/index.html

# ADD same as COPY but can copy from remote and copy tar files

#Set env
ENV key="value" key2="value"

#Change user
USER 1001

#Change work directory
WORKDIR /var/www/html

#Create volume for after use
VOLUME /var/www/html

#Expose port for metadata
EXPOSE 8080

COPY index.html index.html

#Default command, not mandotary
ENTRYPOINT ["/bin/sh","-c"]

#Only last CMD command ll run
CMD ["/bin/httpd","-D","FOREGROUND"]


