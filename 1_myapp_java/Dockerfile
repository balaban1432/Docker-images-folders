FROM ubuntu:18.04
RUN apt-get update -y 
# install java
RUN apt-get install default-jre -y  
WORKDIR /merhaba
COPY ./myapp . 
CMD [ "java", "merhaba" ]