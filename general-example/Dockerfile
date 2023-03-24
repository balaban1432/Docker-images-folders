FROM nginx:latest
LABEL maintainer="ramazan balaban" email="balaban1432@gmail.com"
ENV KULLANICI="Ramazan"
ARG RENK
RUN apt-get update -y && apt-get install curl htop wget -y 
WORKDIR /gecici
ADD https://wordpress.org/latest.tar.gz .
WORKDIR /usr/share/nginx/html
COPY html/${RENK} .
HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD curl -f http://localhost/ || exit 
CMD rm index.html;sed -e s/KULLANICI/"$KULLANICI"/ temp.html > index1.html; sed -e s/HOSTNAME/"$HOSTNAME"/ index1.html > index.html ; nginx -g 'daemon off;'