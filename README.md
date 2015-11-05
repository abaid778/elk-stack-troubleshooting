# elk-stack-troubleshooting

### High CPU Logstash 1.4
This fix is apply on these version logstash 1.4 OS ubuntu 14.04 
* `echo manual | sudo tee /etc/init/logstash-web.override`
To stop logstash-web without rebooting, we use
* `sudo stop logstash-web`

### Memory tunning Elasticsearch 1.5 

Open the `/etc/elasticsearch/elasticsearch.yml` add below line
* `indices.breaker.fielddata.limit: "80%"`
Need to add the variable in the elastic search just type below command and restart the elasticsearch
* `export ES_HEAP_SIZE=6g`
