FROM ubuntu
RUN apt-get update -y
RUN apt-get install python3 -y
RUN apt-get install python3-pip -y
RUN pip3 install flask --break-system-packages
COPY . /app
WORKDIR /app
CMD python3 ./welcome.py
HEALTHCHECK --interval=5m --timeout=3s CMD curl -f http://localhost/ || exit 1