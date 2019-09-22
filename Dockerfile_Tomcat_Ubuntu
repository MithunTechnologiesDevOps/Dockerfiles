FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade \
    && apt-get -y install openjdk-8-jdk wget
RUN mkdir /usr/local/tomcat
RUN wget http://apachemirror.wuchna.com/tomcat/tomcat-8/v8.5.46/bin/apache-tomcat-8.5.46.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz \
    && cp -Rv /tmp/apache-tomcat-8.5.46/* /usr/local/tomcat/
EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run
