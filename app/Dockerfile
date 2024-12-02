FROM python:3.12.3-alpine

WORKDIR /src/app

COPY ./requirements.txt ./requirements.txt

RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

RUN pip3 install --upgrade pip && pip3 install --no-cache-dir --upgrade -r requirements.txt	

COPY . .
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV MY_ENV=crud_18_11_24	

ENTRYPOINT ["/src/app/entrypoint.sh"]

