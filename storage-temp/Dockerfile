FROM zchrhzkl/stf:latest

USER root
WORKDIR /app
RUN mkdir data
RUN chown stf:stf data
USER stf
VOLUME ["data"]
