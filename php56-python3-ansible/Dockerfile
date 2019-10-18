From php:5.6

# 
# Update
RUN apt update

# Install base packages
RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get dist-upgrade --dry-run && \
    apt install git unzip zip vim wget gpg -y && \
    apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev -y

#Install Python
RUN wget https://www.python.org/ftp/python/3.6.9/Python-3.6.9.tgz && \
    tar xvf Python-3.6.9.tgz && \
    cd Python-3.6.9 && \
    ./configure --enable-shared --with-ensurepip=install && \
    make -j8 && \
    make altinstall && \
    alias python3=python3.6

ENV LD_LIBRARY_PATH=/Python-3.6.9/

RUN wget https://bootstrap.pypa.io/get-pip.py  && python3.6 get-pip.py && \
    pip install ansible
