FROM python:3.7

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN uname -a
RUN apt-get update && apt-get -y install vim
RUN apt-get -y install curl
RUN pip3 install requests
RUN pip3 install flask

EXPOSE 5000
CMD ["python", "/app/main.py"]
