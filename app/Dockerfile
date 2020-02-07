FROM python:3.7

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN pip install requests
RUN apt install
RUN pip3 install flask

EXPOSE 5000
CMD ["python", "/app/main.py"]
