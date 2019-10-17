From php:5.6

# 
# Install Needed Packages
RUN apt update && \
    apt-get dist-upgrade --dry-run && \
    apt install git unzip zip vim python3 python3-pip -y && \
    pip3 install ansible
