# patch-elastic
patch bare metal or VM-installed Elastic

## To do

1. use find module to see what role(s) a node has (main.yml) and then add_host module to create groups
  - master
  - transform
  - coordinating
  - logstash
  - machine learning # need to figure out the curl command to stop currently running ML jobs
  - kibana
  - content
  - hot
  - warm
  - cold
  - frozen

2. turn off services in prescribed order
# Top == Stop First --> Bottom == Stop Last
  - machine learning
  - agent
  - beat(s)
  - frozen
  - cold
  - warm
  - hot
  - content 
  - kibana
  - coordinating
  - transform
  - master