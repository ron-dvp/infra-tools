FROM logstash:8.0.0

WORKDIR /usr/share/logstash/bin
RUN logstash-plugin install logstash-input-kinesis
RUN logstash-plugin install logstash-output-coralogix

COPY ./logstash.conf /usr/share/logstash/pipeline/logstash.conf
COPY ./logstash.yml /usr/share/logstash/config/logstash.yml


EXPOSE 9200
EXPOSE 5044