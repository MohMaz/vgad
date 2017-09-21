FROM docker.elastic.co/logstash/logstash:5.5.1
RUN rm -f /usr/share/logstash/pipeline/logstash.conf
ADD logstash-pipelines/ /usr/share/logstash/pipeline/
#ADD config/ /usr/share/logstash/config/
