# mongoDB - watchdog

FROM ptgregistry.corp.intuit.net/ptgrhel65
MAINTAINER PTG Services/PTG-PD Operations

# RUN yum install -y curl tar
# RUN yum clean all

WORKDIR /
RUN curl -O http://apdpdnexus.corp.intuit.net/nexus/content/repositories/platform/com/mongo/mongodb-linux-x86_64/2.6.7/mongodb-linux-x86_64-2.6.7.tgz
RUN mkdir -p /usr/local/mongodb
RUN tar -xvf /mongodb-linux-x86_64-2.6.7.tgz -C /usr/local/mongodb
RUN mv -v /usr/local/mongodb/mongodb-linux-x86_64-2.6.7/* /usr/local/mongodb/
RUN rm -rf /usr/local/mongodb/mongodb-linux-x86_64-2.6.7
RUN rm -rf /mongodb-linux-x86_64-2.6.7.tgz
RUN mkdir /usr/local/mongodb/conf
RUN mkdir /usr/local/mongodb/logs
RUN mkdir -p /usr/local/mongodb/data/db
VOLUME ["/usr/local/mongodb/logs", "/usr/local/mongodb/conf"]
ADD mongodb.conf /usr/local/mongodb/conf/
EXPOSE 21017
ENTRYPOINT /usr/local/mongodb/bin/mongod -f /usr/local/mongodb/conf/mongodb.conf
