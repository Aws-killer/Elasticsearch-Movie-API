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
Example Response
```json
{'_shards': {'failed': 0, 'skipped': 0, 'successful': 1, 'total': 1},
 'hits': {'hits': [{'_id': '2835',
    '_index': 'telegram_media',
    '_score': 7.2320805,
    '_source': {'caption': 'Cars',
     'genres': ['animation', 'comedy', 'family', 'sport'],
     'imageUrl': 'https://m.media-amazon.com/images/M/MV5BMTg5NzY0MzA2MV5BMl5BanBnXkFtZTYwNDc3NTc2._V1_.jpg',
     'imdb_id': 'tt0317219',
     'rating': 7.1,
     'title': 'Cars',
     'type': 'movie'},
    '_type': '_doc',
    'sort': [7.2320805, -9223372036854775808, 'Cars']},

```
Field Definition
* `_id`    Message_id (telegram)
* `_index` Elasticsearch index
* `_score` Search Score 
* `_source` File metadata
  
  


