
# API

- data should be exposed autmatically via REST API

# Admin UI

- need to build an Admin UI (web based) that will provide database management as well as Data Exploration capabilities

# Structure

- since 99.9% of 3.2 billion base pair are identical in every person, it makes sense to chose a "model" or "reference" genome and for other store only the differences.
- the differences could be stored as a hashmap <base pair id, value>
- on WRITE, the values will be comapred with the corresponding values in reference genome and if identical, the value will not be saved If different, the value will be saved to the hashmap
- on READ, the base pair id will be read from the differences hashmap as well, if not found then from the reference genome

# Storage

- should support multiple storages via abstraction + plugin
- Cassandra
- Redis
- Look at how KairosDB and Titan are implemented
