FROM ubuntu:18.04
RUN apt-get update && apt-get install -y python python-pip
RUN pip install --upgrade pip
RUN pip install flask
RUN useradd -ms /bin/bash devopswithcloud
USER devopswithcloud
COPY . /opt/
EXPOSE 8080
ENTRYPOINT FLASK_APP=/opt/app.py flask run --host=0.0.0.0 --port=8080
