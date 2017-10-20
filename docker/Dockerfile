FROM ubuntu:16.04

RUN apt-get update && apt-get install -y --fix-missing \
    gcc mongodb git wkhtmltopdf xvfb python2.7 python-pip \
    python-dev build-essential libssl-dev libffi-dev \
    apache2 libapache2-mod-wsgi

RUN git clone https://github.com/danielpuschmann/bae-charging-backend-test.git

RUN pip install sh

WORKDIR bae-charging-backend-test

RUN git checkout develop

# Create required folders
RUN mkdir -p /data/db/
RUN mkdir ./src/media
RUN mkdir ./src/media/bills
RUN mkdir ./src/media/assets
RUN mkdir ./src/plugins

ENV WORKSPACE=`pwd`

RUN ./python-dep-install.sh

# Create volumes
VOLUME /data/db
VOLUME /bae-charging-backend-test/src/media/bills
VOLUME /bae-charging-backend-test/src/media/assets
VOLUME /bae-charging-backend-test/src/plugins

WORKDIR src

RUN rm wsgi.py
COPY wsgi.py .

WORKDIR /etc/apache2/
COPY charging.conf ./sites-available

RUN ln -s ../sites-available/charging.conf ./sites-enabled/charging.conf
RUN sed -i "s|Listen 80|Listen 8006|g" ports.conf

WORKDIR /bae-charging-backend-test/src

COPY ./entrypoint.sh /

EXPOSE 8006

ENTRYPOINT ["/entrypoint.sh"]

