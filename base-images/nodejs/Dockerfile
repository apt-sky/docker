FROM ptgregistry.corp.intuit.net/ptgrhel65
MAINTAINER PTG Services/PTG-PD Operations

WORKDIR /
ENV http_proxy http://qypprdproxy02.ie.intuit.net:80/
ENV https_proxy http://qypprdproxy02.ie.intuit.net:80/
ENV ftp_proxy http://qypprdproxy02.ie.intuit.net:80/
ENV no_proxy .intuit.com,.ieptc.intuit.net,.qbo.intuit.com,.pharos.intuit.com,.corp.intuit.com,.apddev.intuit.com,.corp.intuit.net,.plano.intuit.com,.qdc.ep.intuit.net,http://www.quickbase.com,.corp.intuit.net,127.0.0.1,localhost,ep.intuit.net,.accountant.intuit.net,.ie.intuit.net
ENV HTTP_PROXY http://qypprdproxy02.ie.intuit.net:80/
ENV HTTPS_PROXY http://qypprdproxy02.ie.intuit.net:80/
ENV FTP_PROXY http://qypprdproxy02.ie.intuit.net:80/

RUN yum install npm -y

RUN unset http_proxy
RUN unset https_proxy
RUN unset ftp_proxy
RUN unset no_proxy
RUN unset HTTP_PROXY
RUN unset HTTPS_PROXY
RUN unset FTP_PROXY
