# syntax=docker/dockerfile:1

FROM python:3.11
LABEL maintainer="pin@to25.ru"

WORKDIR /usr/src/app

#ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/python/app.py \
#/usr/src/app
#ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/python/requirements.txt \
#/usr/src/app

ADD . .

RUN pip install --no-cache-dir -r ./requirements.txt

EXPOSE 8080
ENTRYPOINT python ./app.py
