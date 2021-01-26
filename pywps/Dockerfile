FROM python:3.8-slim

RUN apt update && apt install -y git python3-gdal

RUN git clone git://github.com/geopython/pywps-flask.git pywps-flask

WORKDIR /pywps-flask
RUN pip3 install -r requirements.txt

EXPOSE 5000
ENTRYPOINT ["python", "demo.py","-a"]