# larning-elasticsearch

- 参考
  - https://qiita.com/Esfahan/items/3c07bfbb57c7098e9531
  - https://ishiis.net/2016/09/19/elasticsearch-vagrant/

```bash
curl http://192.168.33.11:9200/_cluster/health?pretty

curl http://192.168.33.11:9200/_cat/nodes

curl http://192.168.33.11:9200/_search?pretty

cat small.json | jq -c '.[] | {"index": {"_index": "bookmarks", "_type": "bookmark" }}, .' | curl -XPOST 192.168.33.11:9200/_bulk?pretty --data-binary @-
```
