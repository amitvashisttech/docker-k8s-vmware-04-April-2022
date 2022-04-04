# Base image
FROM ubuntu:16.04 

# Maintainer of the Image
MAINTAINER Amit <amitvashist7@outlook.com>

# Initialize the APT Repos
RUN apt-get update 

# Install Apache2 Packages 
RUN apt-get install apache2 -y 

# Bring the Service UP
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
