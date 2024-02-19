FROM python:3.8-slim

COPY requirements.txt /
RUN pip install -r /requirements.txt

ADD . /simple_worker
WORKDIR /simple_worker

CMD [ "celery", "-A", "tasks", "worker", "--loglevel=info" ]