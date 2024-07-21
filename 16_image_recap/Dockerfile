FROM nginx:latest
LABEL maintaner="Ramazan Balaban" email="balaban1432@gmail.com"
ENV KULLANICI="Ramazan Balaban"
ARG RENK
RUN apt-get update -y && apt-get install -y curl htop wget
WORKDIR /gecici
ADD https://wordpress.org/latest.tar.gz .
WORKDIR /usr/share/nginx/html
COPY html/${RENK}/ .
HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD curl -f http://localhost/ || exit 1
CMD [ "./script.sh" ]