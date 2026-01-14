The [FASTA](https://en.wikipedia.org/wiki/FASTA_format) format is perhaps the simplest text format for biological sequences that still allow some metadata for the sequence. [NCBI](https://blast.ncbi.nlm.nih.gov/doc/blast-topics/)

The first line is the description line and must start with a greater-than ("**>**") symbol followed by a *name* that can **not** have spaces.
All other lines are assumed to be sequence data. Lower-case letters are accepted and assumed the same as upper-case.
Numbers are not permitted and are filtered by some tools. The sequence ends by a blank line. The sequence data can have
lines of varying length, but no

Sequences are expected to be in the standard [[IUPAC]] amino acid or nucleic acid codes.

Filename extensions ".fasta", ".faa", ".fa", ".fas", and ".fsa" are common for text files containing FASTA sequences.

A DNA sequence:
```
>myDNAname
agctactactgagtcatcgtgtatgcgtatgatcatctatgcgtagtcgtacgtatctattcgatcg
```

A protein sequence:
```
>myprotein_name
MNSERSDVTLYQPFLDYAIAYMRSRLDLEPYPIPTGFESNSAVVGKGKNQEEVVTTSYAFQTAKLRQIRA
AHVQGGNSLQVLNFVIFPHLNYDLPFFGADLVTLPGGHLIALDMQPLFRDDSAYQAKYTEPILPIFHAHQ
QHLSWGGDFPEEAQPFFSPAFLWTRPQETAVVETQVFAAFKDYLKAYLDFVEQAEAVTDSQNLVAIKQAQ
LRYLRYRAEKDPARGMFKRFYGAEWTEEYIHGFLFDLERKLTVVK
```
