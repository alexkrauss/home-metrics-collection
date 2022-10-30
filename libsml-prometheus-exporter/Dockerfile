FROM debian:bullseye-slim
RUN apt-get update && apt-get install libatomic1 && apt-get clean
COPY ./lib /exporter
COPY ./libsml-prometheus-exporter /exporter/libsml-prometheus-exporter
ENV LD_LIBRARY_PATH=/exporter
ENTRYPOINT ["/exporter/libsml-prometheus-exporter"]