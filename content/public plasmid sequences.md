---
publish: true
---

## Plasmid sequence resources

- [Our public plasmid sequences](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences) The **mec collection of plasmid sequence files**, including general yeast vectors and Yeast Pathway Kit plasmids.

- [Addgene](https://www.addgene.org/browse/) Plasmid repository for finding and requesting research plasmids. Browse collections or search by sequence.

- [European Plasmid Repository](https://www.plasmids.eu/) European service for depositing and requesting research plasmids, with support for distribution and Material Transfer Agreements (MTAs).

- [SnapGene plasmid files](https://www.snapgene.com/plasmids) A collection of annotated plasmid maps and downloadable sequence files for common cloning and expression vectors, including yeast plasmids.

- [EUROSCARF](https://www.euroscarf.de/index.php?name=Contact) Yeast strain and plasmid collection, relevant for _Saccharomyces cerevisiae_ research.

- [NBRP Yeast](https://yeast.nig.ac.jp/yeast/top.jsf) Japanese repository of budding- and fission-yeast resources, with plasmid catalogues and maps or sequences where available.

- [DNASU](https://dnasu.org/DNASU/SearchOptions.do) Plasmid repository searchable by gene, clone identifier, or sequence; records include insert sequences and maps where available.

- [NovoPro vector database](https://www.novoprolabs.com/vector/) Collection of plasmid maps and reference sequences compiled from publications and public databases; experimental sequence verification varies.

## Searching for plasmids in GenBank

- [NCBI Nucleotide / GenBank](https://www.ncbi.nlm.nih.gov/nucleotide/) Public sequence database for finding deposited plasmid and cloning-vector sequences by name or accession number.

To find sequences annotated as circular between 2 000 and 20 000 bp, paste this query into NCBI Nucleotide:

```text
2000:20000[SLEN] AND "topology circular"[PROP]
```

[Run this search](https://www.ncbi.nlm.nih.gov/nuccore/?term=2000%3A20000%5BSLEN%5D%20AND%20%22topology%20circular%22%5BPROP%5D). Replace the two numbers to change the length range. `[SLEN]` filters sequence length, and `"topology circular"[PROP]` selects records annotated as circular.

This includes plasmids without requiring them to be classified as plasmids, but can also return viral genomes, mitochondrial sequences, and other circular molecules. Records lacking a circular-topology annotation are excluded.

To restrict the search to records classified as plasmids, add `plasmid[filter]`.

```text
2000:20000[SLEN] AND "topology circular"[PROP] AND plasmid[filter]
```

## Annotation

- [pLannotate](https://plannotate.barricklab.org/) Web tool for annotating engineered plasmid sequences. Accepts FASTA, GenBank, or pasted DNA sequences and provides plasmid maps and downloadable GenBank annotations.
- [PlasMapper 3.0](https://plasmapper.ca/) Web tool for automatically annotating plasmid sequences and generating, editing, and interactively visualizing plasmid maps.
- [Bakta Web](https://bakta.computational.bio/) Web tool for annotating bacterial genomes, metagenome-assembled genomes (MAGs), and plasmids using a curated reference database. Identifies protein-coding genes, RNAs, and other features, with downloadable annotations in GenBank and other formats.
