FROM       nuxeo:8.10
MAINTAINER Nuxeo <packagers@nuxeo.com>

USER root

RUN mkdir /var/lib/nuxeo \
    && chmod a+rw /var/lib/nuxeo \
    && mkdir /var/log/nuxeo \
    && chmod a+rw /var/log/nuxeo \
    && mkdir /var/run/nuxeo \
    && chmod a+rw /var/run/nuxeo \
    && chmod a+rw $NUXEO_HOME \
    && chmod -R a+rw $NUXEO_HOME/* \
    && chmod a+x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh

USER nuxeo

WORKDIR $NUXEO_HOME
COPY docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
EXPOSE 8080
EXPOSE 8787
CMD ["nuxeoctl","console"]
