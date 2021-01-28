FROM python:3.8-slim

# ENV HTTP_PROXY http://bloody_proxy_ip:3128
# ENV HTTPS_PROXY http://bloody_proxy_ip:3128

RUN apt-get update && apt-get install -y git python3-gdal

RUN git clone git://github.com/geopython/pywps-flask.git pywps-flask

WORKDIR /pywps-flask
RUN pip3 install -r requirements.txt

EXPOSE 5000
ENTRYPOINT ["python", "demo.py","-a"]
