# A new method for taxonomic classification using MinHash and Sequence Bloom Trees

- [Luiz Carlos Irber Júnior](https://github.com/luizirber)
- [Philip Brooks](https://github.com/brooksph)
- [Taylor Reiter](https://github.com/taylorreiter)
- [C. Titus Brown](https://github.com/ctb)

- Department of Population Health and Reproduction, University of California, Davis, USA

[Poster][1] and [talk][2] presented at [Bioinformatics for the Microbiome Symposium][3]
at Stanford on 2018-09-24.

## Abstract

We introduce sourmash gather, a new method for taxonomic classification using
MinHash and Sequence Bloom Trees. We ran the NIST-IMMSA benchmark and `gather`
has better precision and recall than other tools.

`gather` uses the same Sequence Bloom Tree index we already use for searching
similar datasets in public databases (like RefSeq and GenBank), but a different
search strategy: instead of looking for all datasets above a similarity
threshold, `gather` does a greedy search for the best match, report it and
then remove the match from the query. This process is repeated while there
are enough items in the query to find matches above a certain threshold.

`gather` is a new feature in sourmash 2.0, available on Bioconda and PyPI.

## References

- Broder, Andrei Z. 1997. “On the Resemblance and Containment of Documents.” - In Compression and Complexity of Sequences 1997. Proceedings, 21–29. IEEE. http://ieeexplore.ieee.org/abstract/document/666900/.
- Ondov, Brian D., Todd J. Treangen, Páll Melsted, Adam B. Mallonee, Nicholas H. Bergman, Sergey Koren, and Adam M. Phillippy. 2016. “Mash: Fast Genome and Metagenome Distance Estimation Using MinHash.” Genome Biology 17: 132. https://dx.doi.org/10.1186/s13059-016-0997-x
- Titus Brown, C., and Luiz Irber. 2016. “sourmash: A Library for MinHash Sketching of DNA.” The Journal of Open Source Software 1 (5). https://dx.doi.org/10.21105/joss.00027


[1]: poster/poster.pdf
[2]: talk.pdf
[3]: https://med.stanford.edu/gbsc/conferences/MicrobiomeSymposium2018.html
