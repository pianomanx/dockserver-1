#####################################
# All rights reserved.              #
# started from Zero                 #
# Docker owned dockserver           #
# Docker Maintainer dockserver      #
#####################################
#####################################
# THIS DOCKER IS UNDER LICENSE      #
# NO CUSTOMIZING IS ALLOWED         #
# NO REBRANDING IS ALLOWED          #
# NO CODE MIRRORING IS ALLOWED      #
#####################################
FROM ghcr.io/squidfunk/mkdocs-material:latest
LABEL maintainer=dockserver
LABEL org.opencontainers.image.source https://github.com/dockserver/dockserver/

COPY ./wiki/requirements.txt /tmp/install.txt
RUN python3 -m pip install --upgrade pip \
    && python3 -m pip install --no-warn-script-location --upgrade --force-reinstall --no-deps --user -r /tmp/install.txt \
    && rm -rf /tmp/* && rm -rf /var/cache/apk/* && rm -rf /tmp/* /root/.cache /root/.lib  /root/.local

WORKDIR /docs

EXPOSE 8000
ENTRYPOINT ["mkdocs"]
CMD ["serve", "--dev-addr=0.0.0.0:8000" ]
