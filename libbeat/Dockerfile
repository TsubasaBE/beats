FROM golang:1.17.8

RUN \
    apt-get update \
      && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
         netcat \
         libpcap-dev \
         python3 \
         python3-pip \
         python3-venv \
      && rm -rf /var/lib/apt/lists/*

RUN pip3 install --upgrade pip==20.1.1
RUN pip3 install --upgrade setuptools==47.3.2
RUN pip3 install --upgrade docker-compose==1.23.2

# Libbeat specific
RUN mkdir -p /etc/pki/tls/certs
