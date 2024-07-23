# ELK_BeginnersGuide

Steps:
1. Install Elastic Search:\
If the version is above 8.0.0, add following line to remove authentication in elasticsearch-x.y.z\config\elasticsearch.yml:\
xpack.security.enabled: false
3. Run **elasticsearch-x.y.z\bin\elasticsearch.bat** and verify if JSON is present on http://localhost:9200/ 
4. Install Kibana of same version\
5. Start with **kibana-x.y.z\bin\kibana.bat** and goto ElasticDashboard on http://localhost:5601/
6. NOTE: Kibana connects to Elastic on http://localhost:9200/ by default

Docker Steps:\
Reference: https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html \
1.Start ElasticSearch (NOT WORKING)
  > docker network create elastic\
  > docker pull docker.elastic.co/elasticsearch/elasticsearch:8.14.3\
  > docker run --name es01 --net elastic -p 9200:9200 -it -m 1GB docker.elastic.co/elasticsearch/elasticsearch:8.14.3\
  > docker cp es01:/usr/share/elasticsearch/config/certs/http_ca.crt .\
  > curl --cacert http_ca.crt -u elastic:<ELASTIC_PASSWORD__PATH> https://localhost:9200
 
