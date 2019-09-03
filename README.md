### ES
##### Healthcheck
curl http://127.0.0.1:9200/_cat/health
##### Create index
curl -X PUT "localhost:9200/twitter?pretty"
##### Add to index
curl -X POST "localhost:9200/twitter/doc/_bulk?pretty" -H 'Content-Type: application/json' -d'
{ "index" : {} }
{ "user" : "kimchy", "post_date" : "2010-11-15T14:00:18", "message" : "Welcome to Aperture science" }
{ "index" : {} }
{ "user" : "kimchy", "post_date" : "2010-11-15T14:12:12", "message" : "My name is GLaDOS" }
'