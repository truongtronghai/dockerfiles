FROM ubuntu

RUN apt update && apt install -y python3

RUN apt install -y python3-pip python3-dev default-libmysqlclient-dev build-essential

RUN apt install -y vim

RUN pip install 'fastapi[all]'

RUN mkdir fastapiapp

WORKDIR /fastapiapp

RUN cd /fastapiapp

COPY main.py main.py

EXPOSE 8000/tcp

CMD ["uvicorn","--host","0.0.0.0","--port","8000","main:app"]