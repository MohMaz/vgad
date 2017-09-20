# How to run:
#### Run  compose file:
```docker-compose -f SingleNode.yml up -d```

#### verify kafka-rest is running:  
```docker logs -f kafka-rest | grep -i "server started"```
  -  restart *kafka-rest* if not running: `docker restart kafka-rest`

#### send simple data to *kafka-rest*:
 
```
curl -X POST -H "Content-Type: application/vnd.kafka.json.v2+json" \
          --data '{"records":[{"value":{"name": "testUser"}}]}' \
          "http://localhost:8082/topics/vgad"
```


