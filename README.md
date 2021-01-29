# Elasticsearch Movie API
Search  API powered by [Elasticsearch](https://github.com/elastic/elasticsearch) for people who want to try out Elasticsearch

<img src="https://images.contentstack.io/v3/assets/bltefdd0b53724fa2ce/blt280217a63b82a734/5bbdaacf63ed239936a7dd56/elastic-logo.svg" width="200" height="100">

Test my API
```python
pip install elasticsearch
```
```python
#Using elasticsearch module
from elasticsearch import Elasticsearch
node_url ='https://public:nhw9pvwcnvjw0klkeulwtxth5zzr1ssi@oin-us-east-1.searchly.com'
es_index_name = 'telegram_media'

es_nodes =[node_url]
es = Elasticsearch(es_nodes)

search_term = "Avengers"
body = {"id": "default_search", "params": {"search_term": search_term}}
es.search_template(index=es_index_name, body=body)
```


