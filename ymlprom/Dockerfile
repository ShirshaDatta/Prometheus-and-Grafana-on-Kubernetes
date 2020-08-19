FROM centos:7
RUN yum install wget -y
RUN wget https://github.com/prometheus/prometheus/releases/download/v2.18.1/prometheus-2.18.1.linux-amd64.tar.gz
RUN tar -xzf prometheus-2.18.1.linux-amd64.tar.gz
RUN mkdir prometheus_data
RUN cp -rvf prometheus-2.18.1.linux-amd64/* /
ENTRYPOINT [ "./prometheus-2.18.1.linux-amd64/prometheus" ]
CMD [ "--storage.tsdb.path='prometheus_data/'","--config.file='/prometheus.yml'" ]
EXPOSE 9090
