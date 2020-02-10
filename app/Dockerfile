FROM python:3.6

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN uname -a
RUN apt-get update & apt-get -y install gcc unzip
RUN apt-get -y install curl
RUN pip3 install requests
RUN pip3 install flask

EXPOSE 5000
CMD ["python", "/app/main.py"]
