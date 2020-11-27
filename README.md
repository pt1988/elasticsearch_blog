# Elasticsearch pitfalls 

## 1. elasticsearch shard limit up to 1000 shards per node by default.

### Solution
```
curl -XPUT 127.0.0.1:9200/_cluster/settings -H "Content-Type: application/json" -d '{   "persistent": { "cluster.max_shards_per_node": "3000"   } }'
```
