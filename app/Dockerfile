FROM python:3.6

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN uname -a
RUN apt-get update
RUN pip install requests
RUN pip3 install flask

EXPOSE 5000
CMD ["python", "/app/main.py"]
