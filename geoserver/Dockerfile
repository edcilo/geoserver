FROM openjdk:8

ENV GEOSERVER_VERSION=2.18.2
ENV GEOSERVER_HOME=/usr/share/geoserver
ENV GEOSERVER_DATA_DIR=/usr/share/geoserver/data_dir

WORKDIR ${GEOSERVER_HOME}

RUN wget --no-check-certificate --progress=bar:force:noscroll \
    https://sourceforge.net/projects/geoserver/files/GeoServer/${GEOSERVER_VERSION}/geoserver-${GEOSERVER_VERSION}-bin.zip \
    && unzip -q geoserver-${GEOSERVER_VERSION}-bin.zip -d ./ \
    && rm geoserver-${GEOSERVER_VERSION}-bin.zip 

RUN chown -R root /usr/share/geoserver

EXPOSE 8080

CMD ["sh", "./bin/startup.sh"]
