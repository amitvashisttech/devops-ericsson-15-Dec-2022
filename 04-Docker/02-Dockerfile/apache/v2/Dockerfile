# Base Image
FROM ubuntu:22.04

# Maintainer
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

# Update the APT Repo
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# App Listen to Port 80
EXPOSE 80

# Bring the Apache Service Up
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"] 
