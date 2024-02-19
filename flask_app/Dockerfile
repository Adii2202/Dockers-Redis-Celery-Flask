FROM python:3.8-slim

COPY requirements.txt /
RUN pip install -r /requirements.txt

#COPY app.py/app.py
ADD . /flask_app
WORKDIR /flask_app

# we exposed the ports in the docker-compose.yaml so here there's no need to do that

ENV FLASK_APP=app.py

CMD ["flask", "run", "--host=0.0.0.0"]