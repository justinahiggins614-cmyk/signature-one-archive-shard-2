# signature-one-archive-shard-2

Data shard for the JAH Spec Catalog. Holds sealed spec chunks
(`data/volumes/specs-cNNNNN.jsonl.gz`) plus the search index the main
catalog page loads (`data/index/specs.idx.json.gz`).

This repo is frozen storage: the main site's page fetches from it directly.
New specs always land in the main repo; when the main repo nears its size
guard, more chunks move to a new shard repo the same way.
