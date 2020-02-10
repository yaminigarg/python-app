FROM python:3.6
RUN apt-get update & apt-get -y install gcc unzip
RUN wget https://releases.hashicorp.com/terraform/0.11.11/terraform_0.11.11_linux_amd64.zip
RUN unzip terraform*
RUN mv terraform /usr/local/bin/
RUN rm -rf terraform*
RUN pip install numpy==1.14.5
RUN pip install setuptools==39.1.0
RUN pip install rasa_nlu==0.13.8
RUN pip install rasa_nlu[spacy]
RUN python -m spacy download en_core_web_sm
RUN python -m spacy link en_core_web_sm en
RUN pip install rasa_core==0.12.3
RUN pip install elasticsearch
RUN pip install msgpack==0.5.6
RUN pip install pandas
RUN pip install xlrd
RUN pip install azure
RUN pip install requests
RUN pip install boto3
COPY . /
RUN python3.6 nlu_model.py
EXPOSE 5005
RUN chmod +x test2.sh
CMD ["sh","-c","./test2.sh && tail -f /dev/null"]
