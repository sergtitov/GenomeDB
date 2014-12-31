
# API

- data should be exposed autmatically via REST API

# Admin UI

Need to build an Admin UI (web based) that will provide:
- database management 
- Data Exploration capabilities
- Import
- Export
- Conversion between different formats

# Structure

- since 99.9% of 3.2 billion base pair are identical in every person, it makes sense to chose a "model" or "reference" genome and for other store only the differences.
- the differences could be stored as a hashmap <base pair id, value>
- on WRITE, the values will be comapred with the corresponding values in reference genome and if identical, the value will not be saved If different, the value will be saved to the hashmap
- on READ, the base pair id will be read from the differences hashmap as well, if not found then from the reference genome

## Compression

- http://arxiv.org/abs/1204.1912
- http://en.wikipedia.org/wiki/Compression_of_Genomic_Re-Sequencing_Data

# Storage

- should support multiple storages via abstraction + plugin
- Cassandra
- Redis
- Look at how KairosDB and Titan are implemented

# Databases

- http://www.genenames.org/useful/genome-databases-and-browsers
- http://useast.ensembl.org/downloads.html?redirect=no

# Services and Companies

- [Google Genomics](https://cloud.google.com/genomics/)
- [Seven Bridges](https://www.sbgenomics.com)
- [Tute Genomics](http://tutegenomics.com)
- [Next Code](https://www.nextcode.com/products-and-services/platform-capabilities-and-services#our-services)
- [DNA Nexus](https://www.dnanexus.com)
- [Arvados](https://arvados.org)

# Solutions & Tools

- [Arvados](https://arvados.org)
- [UCSC Genome Browser](https://genome-store.ucsc.edu)
- [Adam](https://github.com/bigdatagenomics/adam), http://www.eecs.berkeley.edu/Pubs/TechRpts/2013/EECS-2013-207.html
- [Arvados](https://github.com/curoverse/arvados)
- [Links](http://www.genomespace.org/support/tools)

# Press

- http://rt.com/news/203463-google-store-human-genome/
- http://www.technologyreview.com/news/532266/google-wants-to-store-your-genome/
- http://www.xconomy.com/boston/2013/12/18/curoverse-gets-1-5m-develop-open-source-genomics-tool/
