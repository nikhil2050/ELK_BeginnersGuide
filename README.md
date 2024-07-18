# ELK_BeginnersGuide

Steps:
1. Install Elastic Search:\
If the version is above 8.0.0, add following line to remove authentication in elasticsearch-x.y.z\config\elasticsearch.yml:\
xpack.security.enabled: false
3. Start elasticsearch-x.y.z\bin\elasticsearch.bat and verify if JSON is present on http://localhost:9200/ 
4. Install Kibana of same version\
5. Start with kibana-x.y.z\bin\kibana.bat and goto ElasticDashboard on http://localhost:5601/
6. NOTE: Kibana connects to Elastic on http://localhost:9200/ by default
