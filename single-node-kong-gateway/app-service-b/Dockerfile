# Dockerfile

FROM python:3.7.3-slim

COPY requirements.txt ./
RUN python3 -m pip install -r requirements.txt

WORKDIR /app

COPY . /app

CMD [ "gunicorn", "-w" , "1", "-b", ":8001", "app:application" ]