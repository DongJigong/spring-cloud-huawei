FROM openjdk:8-jre-alpine
ENV APP_ROOT=/root/servicestage/ticket/
ENV LOG_ROOT=/var/log/ticket/
RUN mkdir -p $APP_ROOT
RUN mkdir -p $LOG_ROOT

COPY target/ticket-1.3.3-Hoxton-SNAPSHOT/ticket-1.3.3-Hoxton-SNAPSHOT $APP_ROOT


RUN cd $APP_ROOT && chmod -R 770 .
RUN chmod +x /root/servicestage/ticket/bin/start.sh

ENTRYPOINT ["sh", "/root/servicestage/ticket/bin/start.sh"]
