# Log-Exporter

This stack deploys the necessary infrastructure for log collection.
It consists of the following components:

* `logstash-collector`: receives logs and forwards to Redis
* `logspout`: runs on host, detects new Docker containers, and forwards console output to `logstash-collector`
* `logstash-lb`: load balancer that opens TCP port for non-container applications to send logs to `logstash-collector`.
