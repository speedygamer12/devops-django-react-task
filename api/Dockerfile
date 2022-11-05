FROM python:3.9-slim-buster

WORKDIR /app


COPY requirements.txt /app

RUN apt update  && \
    apt install -y python3-dev libpq-dev && \
    pip3 install -r requirements.txt

COPY . /app 

ENTRYPOINT ["python3"] 

EXPOSE 8000

CMD ["manage.py", "runserver", "0.0.0.0:8000"]


