# A new method for taxonomic classification using MinHash and Sequence Bloom Trees

Luiz Carlos Irber Junior
Philip Brooks
Taylor Reiter
C. Titus Brown

We introduce sourmash gather, a new method for taxonomic classification using MinHash and Sequence Bloom Trees. We ran the McIntyre benchmark and `gather` has better precision and recall than other tools.

`gather` uses the same Sequence Bloom Tree index we already use for searching similar datasets in public databases (like RefSeq and GenBank), but a different search strategy: instead of looking for all datasets above a similarity threshold, `gather` does a greedy search for the best match, report it and then remove the match from the query. This process is repeated while there are enough items in the query to find matches above a certain threshold.

`gather` is a new feature in sourmash 2.0, available on Bioconda and PyPI.