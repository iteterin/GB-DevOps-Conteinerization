# syntax=docker/dockerfile:1

FROM python:3.11-slim
LABEL maintainer="pin@to25.ru"

WORKDIR /usr/src/app

COPY ./requirements.txt ./

RUN pip install --no-cache-dir -r ./requirements.txt
RUN rm -f ./requirements.txt 

COPY ./app.py ./

EXPOSE 8080
ENTRYPOINT python ./app.py