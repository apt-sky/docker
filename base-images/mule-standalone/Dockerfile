# mule - standalone

FROM ptgregistry.corp.intuit.net/ptg_java:1.8.0

RUN yum install unzip -y
RUN yum clean all
ENV JAVA_HOME /usr/java/default
WORKDIR /
COPY ./mule-standalone-3.6.0.zip /mule-standalone-3.6.0.zip
RUN unzip /mule-standalone-3.6.0.zip
RUN rm -rf /mule-standalone-3.6.0.zip
RUN  mv -v ./mule-standalone-3.6.0 /usr/local/mule-standalone-3.6.0
ENTRYPOINT /usr/local/mule-standalone-3.6.0/bin/mule
