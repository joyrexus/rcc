# Internal Project Development

We aim provide front-end tools for RCC end users in the following areas:

* quota monitoring/management
* job submission/monitoring/management
* resource utilization reporting


## Resources

We're going to investigate an elasticsearch setup with logstash as a backend
aggregator and kibana as the frontend rendering tool.

Using Elasticsearch as a backend datastore, and kibana as a frontend reporting
tool, Logstash acts as the workhorse, creating a powerful pipeline for storing,
querying and analyzing your logs. 

* [kibana](http://www.elasticsearch.org/guide/en/kibana/current/) - kibana docs
* [logstash](http://logstash.net/docs/1.4.2/tutorials/getting-started-with-logstash) - getting started guide


#### Existing RCC monitoring tools

* [graphite-rcc](http://graphite.rcc.uchicago.edu/) - our graphite frontend
* [stats-rcc](http://stats.rcc.uchicago.edu) - various reporting frontends
* [grafana-rcc](http://stats.rcc.uchicago.edu/grafana/#/dashboard/elasticsearch/Slurm%20Cluster%20Usage) - our grafana frontend
