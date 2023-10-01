# syntax=docker/dockerfile:1

FROM python:3.9.6-alpine3.14
LABEL maintainer="pin@to25.ru"

WORKDIR /usr/src/app

COPY ./requirements.txt ./

RUN pip install --no-cache-dir -r ./requirements.txt && rm -f ./requirements.txt 

COPY ./app.py ./

EXPOSE 8080
ENTRYPOINT ["python", "./app.py"]

HEALTHCHECK CMD curl --fail http://localhost:8080 || exit 1