FROM ubuntu:14.04
MAINTAINER Sneha Yadav
RUN apt-get update -y &&\
    apt-get upgrade -y &&\
    apt-get install -y software-properties-common &&\
    add-apt-repository ppa:webupd8team/java -y &&\
    apt-get update &&\
    echo "oracle-java8-installer shared/accepted-oracle-license-v1-1 select true" | sudo /usr/bin/debconf-set-selections &&\
    apt-get install -y oracle-java8-installer &&\
    apt-get clean
COPY . /var/www/java
WORKDIR var/www/java
RUN javac Hello.java
CMD ["java","Hello"]
