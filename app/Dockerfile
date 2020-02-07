FROM python:3.7

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN python -m pip install --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --trusted-host pypi.org --upgrade pip
RUN pip install -r requirements.txt

EXPOSE 5000
CMD ["python", "/app/main.py"]
