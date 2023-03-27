FROM python:alpine
# COPY . /app
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
EXPOSE 80
CMD python bookstore-api.py