FROM odoo:11.0
MAINTAINER <support@savoirfairelinux.com> Savoir-faire Linux Inc

ENV DOCKERIZE_VERSION v0.6.1
ENV COVERAGE_VERSION 4.5.1
ENV CODACY_COVERAGE_VERSION 1.3.11

USER root

RUN set -x; \
    apt-get update && \
    apt-get install -y python3-dev gcc && \
    pip3 install coverage==$COVERAGE_VERSION && \
    pip3 install codacy-coverage==$CODACY_COVERAGE_VERSION && \
    apt-get remove -y python3-dev gcc && \
    apt-get install git -y && \
    apt-get autoremove -y && \
    apt-get clean all && \
    curl -SL https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz | tar xzf - -C /usr/bin

USER odoo
