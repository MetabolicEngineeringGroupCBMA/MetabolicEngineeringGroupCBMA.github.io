This document describes the _dnaudit_ standard for documentation of genetic constructs in a light plain text format and a a combination of yaml, markdown and Genbank files.

The goal of this standard is to facilitate documentation that is clear and unambiguous, yet with minimal markup.

The documentation generated using this standard shows step-by step how a genetic construct was made so that it can be reproduced
while at the same time making it easier to *preserve* and *share* genetic material.

A genetic construct can be for example:

- a plasmid made from parts of other plasmids or chromosomal DNA fragments
- DNA integrated in the genome of an organism by CRISPr

The documentation for a genetic construct consists of a a collection of text files in a folder 📁 with optional sub folders.
Each text file contains a description of a molecular biology [unit-operations](https://en.wikipedia.org/wiki/Unit_operation) consisting of sequences in FASTA format.

A very reduced, easy to remember collection of key words describe each unit-operation. Examples of unit operation are for
example PCR and homologous recombination.

A unit operation is delineated by a header (Table #1) and the next header or the end of the text file.

A unit operation contains a series of input sequences in a specified order as well as at least one resulting sequence.
The file can (and should) also contain comments explaining the aim of the experiment.

| Table#1 | Header         | Unit operation                                             |
| ------- | -------------- | ---------------------------------------------------------- |
|         | `# pcr`        | PCR reaction                                               |
|         | `# cut`        | Restriction digestion with one or more restriction enzymes |
|         | `# crispr`     | CRISPr digestion                                           |
|         | `# ligation`   | Ligation with a DNA ligase                                 |
|         | `# assembly`   | Homologous recombination                                   |
|         | `# fusion_pcr` | fusion PCR                                                 |
|         | `# gateway`    | gateway cloning                                            |

🔑 Additionally, there are some reserved key/value expressions (Table#2) with special meaning.

🚨Key/Value Pairs should contain no white space characters.

| Table#2 | Reserved Key/Value Pairs   | Meaning                                | Note                                                                                              |     |
| ------- | -------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------- | --- |
|         | `cdseguid=...`             | Checksum for a circular dsDNA sequence | Implies a circular molecule even in the absence of `topology=...`                                 |     |
|         | `ldseguid=...`             | Checksum for a linear dsDNA sequence   | Implies a linear molecule even in the absence of `topology=...`                                   |     |
|         | `csseguid=...`             | Checksum for a circular ssDNA sequence | Implies a circular molecule even in the absence of `topology=...`                                 |     |
|         | `lsseguid=...`             | Checksum for a linear ssDNA sequence   | Implies a linear molecule even in the absence of `topology=...`                                   |     |
|         | `alphabet=dsIUPAC`         | Symbols are [[dsIUPAC]].               | This is the default DNA symbol table. This is a super set of the extended [[IUPAC]] nomenclature. |     |
|         | `topology=circular/linear` | Molecule is either circular or linear  |                                                                                                   |     |
|         | `molecule=protein/DNA/RNA` | Indicating a protein sequence.         |                                                                                                   |     |

These reserved Key/Value should be placed after the identifier in the FASTA header.

## Constraints

1. All relevant files have to be in the same project folder tree.
2. Unit-operation snippets must have a .md extension.
3. A unit-operation starts with one of the reserved words from Table#1 or optionally yaml front matter.
4. Sequences in the unit-operation files must be in FASTA [[GenBank\|format]].
5. File names must be unique in the project folder tree.
6. Sequences are identified by their name (This is *not* necessarily the same as the file name of a sequence file).
7. There can be only one identifier for a certain DNA sequence in the project folder.

The [PydnaWeb](https://pydna.pythonanywhere.com) simulation tools can be helpful when preparing unit-operation snippets.
## Examples:



```
---
limit: 13
---

# pcr

This element describe a PCR product for in a yeast gene knockout cassette.

>1776_rv_ERG10_KanMX_del (forward primer)
TGTATTTTATGAAAAAGATCATGAGAAAATCGCAGAACGTAATCAgcataggccactagtggatctg

>1775_fw_ERG10_KanMX_del (reverse primer)
GCGCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGcagctgaagcttcgtacgc

>AJ002680 topology=circular (template)
gaacgcggccgccagctgaagcttcgtacgctgcaggtcgacggatccccgggttaattaaggcgcgccagatctgtttagcttgcctcgtccccgccgggtcacccggccagcgacatggaggcccagaataccctccttgacagtcttgacgtgcgcagctcaggggcatgatgtgactgtcgcccgtacatttagcccatacatccccatgtataatcatttgcatccatacattttgatggccgcacggcgcgaagcaaaaattacggctcctcgctgcagacctgcgagcagggaaacgctcccctcacagacgcgttgaattgtccccacgccgcgcccctgtagagaaatataaaaggttaggatttgccactgaggttcttctttcatatacttccttttaaaatcttgctaggatacagttctcacatcacatccgaacataaacaaccatgggtaaggaaaagactcacgtttcgaggccgcgattaaattccaacatggatgctgatttatatgggtataaatgggctcgcgataatgtcgggcaatcaggtgcgacaatctatcgattgtatgggaagcccgatgcgccagagttgtttctgaaacatggcaaaggtagcgttgccaatgatgttacagatgagatggtcagactaaactggctgacggaatttatgcctcttccgaccatcaagcattttatccgtactcctgatgatgcatggttactcaccactgcgatccccggcaaaacagcattccaggtattagaagaatatcctgattcaggtgaaaatattgttgatgcgctggcagtgttcctgcgccggttgcattcgattcctgtttgtaattgtccttttaacagcgatcgcgtatttcgtctcgctcaggcgcaatcacgaatgaataacggtttggttgatgcgagtgattttgatgacgagcgtaatggctggcctgttgaacaagtctggaaagaaatgcataagcttttgccattctcaccggattcagtcgtcactcatggtgatttctcacttgataaccttatttttgacgaggggaaattaataggttgtattgatgttggacgagtcggaatcgcagaccgataccaggatcttgccatcctatggaactgcctcggtgagttttctccttcattacagaaacggctttttcaaaaatatggtattgataatcctgatatgaataaattgcagtttcatttgatgctcgatgagtttttctaatcagtactgacaataaaaagattcttgttttcaagaacttgtcatttgtatagtttttttatattgtagttgttctattttaatcaaatgttagcgtgatttatattttttttcgcctcgacatcatctgcccagatgcgaagttaagtgcgcagaaagtaatatcatgcgtcaatcgtatgtgaatgctggtcgctatactgctgtcgattcgatactaacgccgccatccagtgtcgaaaacgagctcgaattcatcgatgatatcagatccactagtggcctatgcggccgcggatctgccggtctccctatagtgagtcgtattaatttcgataagccaggttaacctgcattaatgaatcggccaacgcgcggggagaggcggtttgcgtattgggcgctcttccgcttcctcgctcactgactcgctgcgctcggtcgttcggctgcggcgagcggtatcagctcactcaaaggcggtaatacggttatccacagaatcaggggataacgcaggaaagaacatgtgagcaaaaggccagcaaaaggccaggaaccgtaaaaaggccgcgttgctggcgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcaatgctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaaggacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctacggggtctgacgctcagtggaacgaaaactcacgttaagggattttggtcatgagattatcaaaaaggatcttcacctagatccttttaaattaaaaatgaagttttaaatcaatctaaagtatatatgagtaaacttggtctgacagttaccaatgcttaatcagtgaggcacctatctcagcgatctgtctatttcgttcatccatagttgcctgactccccgtcgtgtagataactacgatacgggagggcttaccatctggccccagtgctgcaatgataccgcgagacccacgctcaccggctccagatttatcagcaataaaccagccagccggaagggccgagcgcagaagtggtcctgcaactttatccgcctccatccagtctattaattgttgccgggaagctagagtaagtagttcgccagttaatagtttgcgcaacgttgttgccattgctacaggcatcgtggtgtcacgctcgtcgtttggtatggcttcattcagctccggttcccaacgatcaaggcgagttacatgatcccccatgttgtgcaaaaaagcggttagctccttcggtcctccgatcgttgtcagaagtaagttggccgcagtgttatcactcatggttatggcagcactgcataattctcttactgtcatgccatccgtaagatgcttttctgtgactggtgagtactcaaccaagtcattctgagaatagtgtatgcggcgaccgagttgctcttgcccggcgtcaatacgggataataccgcgccacatagcagaactttaaaagtgctcatcattggaaaacgttcttcggggcgaaaactctcaaggatcttaccgctgttgagatccagttcgatgtaacccactcgtgcacccaactgatcttcagcatcttttactttcaccagcgtttctgggtgagcaaaaacaggaaggcaaaatgccgcaaaaaagggaataagggcgacacggaaatgttgaatactcatactcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacatatttgaatgtatttagaaaaataaacaaataggggttccgcgcacatttccccgaaaagtgccacctgacgtctaagaaaccattattatcatgacattaacctataaaaataggcgtatcacgaggccctttcgtctcgcgcgtttcggtgatgacggtgaaaacctctgacacatgcagctcccggagacggtcacagcttgtctgtaagcggatgccgggagcagacaagcccgtcagggcgcgtcagcgggtgttggcgggtgtcggggctggcttaactatgcggcatcagagcagattgtactgagagtgcaccatatggacatattgtcgttagaacgcggctacaattaatacataaccttatgtatcatacacatacgatttaggtgacactata

>1635bp_PCR_prod (this is the cassette pcr product)
GCGCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGCAGCTGAAGCTTCGTACGCTGCAGGTCGACGGATCCCCGGGTTAATTAAGGCGCGCCAGATCTGTTTAGCTTGCCTCGTCCCCGCCGGGTCACCCGGCCAGCGACATGGAGGCCCAGAATACCCTCCTTGACAGTCTTGACGTGCGCAGCTCAGGGGCATGATGTGACTGTCGCCCGTACATTTAGCCCATACATCCCCATGTATAATCATTTGCATCCATACATTTTGATGGCCGCACGGCGCGAAGCAAAAATTACGGCTCCTCGCTGCAGACCTGCGAGCAGGGAAACGCTCCCCTCACAGACGCGTTGAATTGTCCCCACGCCGCGCCCCTGTAGAGAAATATAAAAGGTTAGGATTTGCCACTGAGGTTCTTCTTTCATATACTTCCTTTTAAAATCTTGCTAGGATACAGTTCTCACATCACATCCGAACATAAACAACCATGGGTAAGGAAAAGACTCACGTTTCGAGGCCGCGATTAAATTCCAACATGGATGCTGATTTATATGGGTATAAATGGGCTCGCGATAATGTCGGGCAATCAGGTGCGACAATCTATCGATTGTATGGGAAGCCCGATGCGCCAGAGTTGTTTCTGAAACATGGCAAAGGTAGCGTTGCCAATGATGTTACAGATGAGATGGTCAGACTAAACTGGCTGACGGAATTTATGCCTCTTCCGACCATCAAGCATTTTATCCGTACTCCTGATGATGCATGGTTACTCACCACTGCGATCCCCGGCAAAACAGCATTCCAGGTATTAGAAGAATATCCTGATTCAGGTGAAAATATTGTTGATGCGCTGGCAGTGTTCCTGCGCCGGTTGCATTCGATTCCTGTTTGTAATTGTCCTTTTAACAGCGATCGCGTATTTCGTCTCGCTCAGGCGCAATCACGAATGAATAACGGTTTGGTTGATGCGAGTGATTTTGATGACGAGCGTAATGGCTGGCCTGTTGAACAAGTCTGGAAAGAAATGCATAAGCTTTTGCCATTCTCACCGGATTCAGTCGTCACTCATGGTGATTTCTCACTTGATAACCTTATTTTTGACGAGGGGAAATTAATAGGTTGTATTGATGTTGGACGAGTCGGAATCGCAGACCGATACCAGGATCTTGCCATCCTATGGAACTGCCTCGGTGAGTTTTCTCCTTCATTACAGAAACGGCTTTTTCAAAAATATGGTATTGATAATCCTGATATGAATAAATTGCAGTTTCATTTGATGCTCGATGAGTTTTTCTAATCAGTACTGACAATAAAAAGATTCTTGTTTTCAAGAACTTGTCATTTGTATAGTTTTTTTATATTGTAGTTGTTCTATTTTAATCAAATGTTAGCGTGATTTATATTTTTTTTCGCCTCGACATCATCTGCCCAGATGCGAAGTTAAGTGCGCAGAAAGTAATATCATGCGTCAATCGTATGTGAATGCTGGTCGCTATACTGCTGTCGATTCGATACTAACGCCGCCATCCAGTGTCGAAAACGAGCTCGAATTCATCGATGATATCAGATCCACTAGTGGCCTATGCTGATTACGTTCTGCGATTTTCTCATGATCTTTTTCATAAAATACA

```



```

---
enzymes: BamHI
---

# cu

Restriction enzyme names such as BamHI or HindIII must be written as they
appear in [rebase](http://rebase.neb.com/rebase/rebase.html).

>sequence1 lsseguid=4Qz0WrmZE8sUTteT11fZBT6dCUE
acgtatctataggatcctcgtattatcgta

>fragment1 alphabet=dsIUPAC
acgtatctatagQFZJ

>fragment2 alphabet=dsIUPAC
PEXIgatcctcgtattatcgta


					Double stranded representation of sequence1
					acgtatctataggatcctcgtattatcgta
					||||||||||||||||||||||||||||||
					TGCATAGATATCCTAGGAGCATAATAGCAT

					            gatcctcgtattatcgta fragment2
					                ||||||||||||||
					                GAGCATAATAGCAT
		  fragment1 acgtatctatag
					||||||||||||
					TGCATAGATATCCTAG

					            PEXIctcgtattatcgta fragment2
	      fragment1 acgtatctatagQFZJ

```





```
# ligate

This snippet describes a cut&ligate cloning procedure. The pwpwq3 PCR product is cloned in the EcoRV site of vector pUCmuK.
This is a blunt cloning and the PCR product is *not* digested with any restriction enzyme.
Restriction enzymes has to
Sequence immediately following the restriction enzyme.
It is important to note that circular topology for FASTA sequences are indicated by `circular` in the header line.

>pwpwq3 ldseguid=l8OpUk_5XHWeEKoduaByO-ZRcbs (this is the insert, linear dsDNA)
gatcGGATCCATGAACTCATATCACATTTGCTTCAACGACTGCCGCCTTCGCTGTATCCCTAGACACTCAACATAAGGATCTatc

>pUCmuK cdseguid=r3Oi6LjFyOLB64eWO2Q-LeRtyq0 cut=EcoRV (this is a circular ds DNA vector)
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagaggatcccgggtaccgagctcgaattcggatatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttaccca

>pUCmuK_pwpwq3 cdseguid=fk6zm54GgaVFAhbvA11wZxEaQ_8 (this is the resulting circular plasmid)
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagaggatcccgggtaccgagctcgaattcggatgatcGGATCCATGAACTCATATCACATTTGCTTCAACGACTGCCGCCTTCGCTGTATCCCTAGACACTCAACATAAGGATCTatcatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttaccca

>myp protein=true (this is an optional protein expressed from the sequence immediately above)
MNSYHICFNDCRLRCIPRHST*



# ligate

This is a sticky end cloning. The pwpwq3 PCR product digested with BamHI & XhoII and
cloned in the BamHI site of vector pUCmuK.

>pwpwq3 linear ldseguid=O8pSBFI3EqOsXu9_a1235LCh9O8 (this is the insert)
LEOFCATGAACTCATATCACATTTGCTTCAACGACTGCCGCCTTCGCTGTATCCCTAGACACTCAACATAQZPX

>pUCmuK circular (this is the vector) cdseguid=r3Oi6LjFyOLB64eWO2Q-LeRtyq0 cut=BamHI
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagaggatcccgggtaccgagctcgaattcggatatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttaccca

>pUCmuK_pwpwq3_sticky cdseguid=sdtvgK1IVf-Jtc6rzS0WJpLG4C0 (this is the resulting vector)
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagagGATCCATGAACTCATATCACATTTGCTTCAACGACTGCCGCCTTCGCTGTATCCCTAGACACTCAACATAAgatcccgggtaccgagctcgaattcggatatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttaccca
```


### homologous recombination

```
# homologous_recombination

This element describes a recombination between the two previous linear PCR products forming a new circular plasmid.

 -|808bp_PCR_prod|27
|                 \/
|                 /\
|                 27|867bp_PCR_pro_rc|30
|                                     \/
|                                     /\
|                                     30-
|                                        |
 ----------------------------------------


>808bp_PCR_prod ldseguid=Dz3zSkRgSWMrtc0AGAZf-lFpbYQ (one DNA fragment)
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagaggatcccgggtaccgagctcgaattcggatatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttcta

>867bp_PCR_prod ldseguid=8cjo-NQlkgLkuRlwS1qT-N10OTk (another DNA fragment)
atgcttcaataatattgaaaaaggaagagtatgggtaaggaaaagactcacgtttcgaggccgcgattaaattccaacatggatgctgatttatatgggtataaatgggctcgcgataatgtcgggcaatcaggtgcgacaatctatcgattgtatgggaagcccgatgcgccagagttgtttctgaaacatggcaaaggtagcgttgccaatgatgttacagatgagatggtcagactaaactggctgacggaatttatgcctcttccgaccatcaagcattttatccgtactcctgatgatgcatggttactcaccactgcgatccccggcaaaacagcattccaggtattagaagaatatcctgattcaggtgaaaatattgttgatgcgctggcagtgttcctgcgccggttgcattcgattcctgtttgtaattgtccttttaacagcgatcgcgtatttcgtctcgctcaggcgcaatcacgaatgaataacggtttggttgatgcgagtgattttgatgacgagcgtaatggctggcctgttgaacaagtctggaaagaaatgcataagcttttgccattctcaccggattcagtcgtcactcatggtgatttctcacttgataaccttatttttgacgaggggaaattaataggttgtattgatgttggacgagtcggaatcgcagaccgataccaggatcttgccatcctatggaactgcctcggtgagttttctccttcattacagaaacggctttttcaaaaatatggtattgataatcctgatatgaataaattgcagtttcatttgatgctcgatgagtttttctaatagaaaagatcaaaggatcttcttgag

>pUCmuK cdseguid=r3Oi6LjFyOLB64eWO2Q-LeRtyq0 (the resulting final plasmid )
actcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacataacgcgtcgcgaggccatatgggttaacccatggccaagcttgcatgcctgcaggtcgactctagaggatcccgggtaccgagctcgaattcggatatcctcgagactagtgggcccgtttaaacacatgtgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaagaacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttaccca




# homologous_recombination

This snippet describes the recombination between the ERG10 locus and the cassette.
Note that the locus sequence is repeated. This is necessary for technical reasons and has to do with how the
internals of the Pydna Assembly class.

ERG10_locus|45
            \/
            /\
            45|1635bp_PCR_prod|45
                               \/
                               /\
                               45|ERG10_locus

>ERG10_locus lSEGUID
ATTGAAGCACCTGTGGAGTATTTAAAAACTGCGGTTACATGGCCTACAGATGAAATATGTGCTCAACTAATGACACAATTCCCACCAGGAACGCCGACCAGTGTCCTGCTGCAGACTATTTCAGATGAGCTAGAGAAAAGTTCTGACAACCTGTTCACGTTATCTGATTTAAAGAGCAAACTGAAAGTTATTGGCTTATTCGAGCACATGGAAGATATCCCATTTTTCGACAAGCTGAAACTAAGCAATGCGCCCGTGAAGGACATGCCTATGGTCACAAAGGCGTTCACCAAATTTTGCGAAACAATAGCAAAAAGGCATACAAGAGGCCTACTGTCATACCGATTACCTTTTAACCTACTGGACTACAATTGCATACCGAATGAGAGTTATTCATTAGAGGTTTATGAGTCATTGTACAACATCATTACTCTATACTTCTGGCTCAGCAACAGGTACCCAAACTACTTCATTGACATGGAATCTGCTAAAGATTTGAAGTATTTCTGTGAGATGATTATTTTCGAGAAACTTGATCGATTAAAGAAGAATCCTTACGCACATAAGCCCTTTGGTTCTACAAGAGGTCACCTCTCATCTTCGAGAAGAAGATTGCGTACATAATCTACGATATATCCTGTAAATAGAAACAGCTACACTGCTTGAAAGCCTTAACATGATACATTTCTGGTATGATGCCATTGTTGTGCCCTGCCGGGTTTATCGTTTCCTAACAGGCACGTCACTTATAACGAGGTGCCTGTCGTTTACCGCCCAAGCCGGTTTTTTCGCTGGAGAGTACGGTACTACTAGCCCACCACACGTTCGTGGCCAGGTTGATAGGCCACCGTTGAGCAAAGGGCAGTAAAATATATAAAAGAGGAACAAGCGCTTCCATTAAGAGCACTGCTAAGCCTACTCGTTTTCTAGTTCTCTGAAAAAAGGTAGCCTAAAACAAGCGCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGTCTCAGAACGTTTACATTGTATCGACTGCCAGAACCCCAATTGGTTCATTCCAGGGTTCTCTATCCTCCAAGACAGCAGTGGAATTGGGTGCTGTTGCTTTAAAAGGCGCCTTGGCTAAGGTTCCAGAATTGGATGCATCCAAGGATTTTGACGAAATTATTTTTGGTAACGTTCTTTCTGCCAATTTGGGCCAAGCTCCGGCCAGACAAGTTGCTTTGGCTGCCGGTTTGAGTAATCATATCGTTGCAAGCACAGTTAACAAGGTCTGTGCATCCGCTATGAAGGCAATCATTTTGGGTGCTCAATCCATCAAATGTGGTAATGCTGATGTTGTCGTAGCTGGTGGTTGTGAATCTATGACTAACGCACCATACTACATGCCAGCAGCCCGTGCGGGTGCCAAATTTGGCCAAACTGTTCTTGTTGATGGTGTCGAAAGAGATGGGTTGAACGATGCGTACGATGGTCTAGCCATGGGTGTACACGCAGAAAAGTGTGCCCGTGATTGGGATATTACTAGAGAACAACAAGACAATTTTGCCATCGAATCCTACCAAAAATCTCAAAAATCTCAAAAGGAAGGTAAATTCGACAATGAAATTGTACCTGTTACCATTAAGGGATTTAGAGGTAAGCCTGATACTCAAGTCACGAAGGACGAGGAACCTGCTAGATTACACGTTGAAAAATTGAGATCTGCAAGGACTGTTTTCCAAAAAGAAAACGGTACTGTTACTGCCGCTAACGCTTCTCCAATCAACGATGGTGCTGCAGCCGTCATCTTGGTTTCCGAAAAAGTTTTGAAGGAAAAGAATTTGAAGCCTTTGGCTATTATCAAAGGTTGGGGTGAGGCCGCTCATCAACCAGCTGATTTTACATGGGCTCCATCTCTTGCAGTTCCAAAGGCTTTGAAACATGCTGGCATCGAAGACATCAATTCTGTTGATTACTTTGAATTCAATGAAGCCTTTTCGGTTGTCGGTTTGGTGAACACTAAGATTTTGAAGCTAGACCCATCTAAGGTTAATGTATATGGTGGTGCTGTTGCTCTAGGTCACCCATTGGGTTGTTCTGGTGCTAGAGTGGTTGTTACACTGCTATCCATCTTACAGCAAGAAGGAGGTAAGATCGGTGTTGCCGCCATTTGTAATGGTGGTGGTGGTGCTTCCTCTATTGTCATTGAAAAGATATGATTACGTTCTGCGATTTTCTCATGATCTTTTTCATAAAATACATAAATATATAAATGGCTTTATGTATAACAGGCATAATTTAAAGTTTTATTTGCGATTCATCGTTTTTCAGGTACTCAAACGCTGAGGTGTGCCTTTTGACTTACTTTTCCGCCTTGGCAAGCTGGCCGGGTGATACTTGCACAAGTTCCACTAATTACTGACATTTGTGGTATTAACTCGTTTGACTGCTCTACAATTGTAGGATGTTAATCAATGTCTTGGCTGCCTTCATTCTCTTCAGGCTCTATTAATTTTAACCGTTATAAGTTCCTTTTCTCCCTTGGAAGCAAACATCAACTGCCTTAAAATCTGGTGGCGAGGAAAGAGGAAATGGCATGTACTAATGATGGTCCTAATAAATATCCCGAAATTGTGAGTGTTAAGCACCTGTTCCAACATTCGGGATCCAAGCATGAATTTAGTGCTGGTAAACGATTTTCAAAATCCATTGGTAAAATATTCAAACGAAACTCTGCTTTGAAAACTTCTAGAACTGAAACGGCAAATCATAAAATGGAATTGAAAAAAAGAGAGGGTGTTACCTTATTGCCACCTGTCCCAGAATCATTATTACATAAACTCAATTCTTGGTTGGAAACTTTTTCTTCCACCAAGAACATGAAAATCGAAGAAAACAAAATTGTTATTAATGAAAAAGAGATTCGGGATTCAGTCTCTTACTACCCTGATAAGAATGGAGGAAGTGCTGTATTTTGTTACTTGCCCGACCTTGTGCTATATTATAAGCCGCCTATAAAAGTCACAGGCAAGCAATGTCCAATAAAGAGAAGTCCTTGGGAATCGATGGAAATCCAATATCAAAAGTTTATGTACCCCTTAGAAAGGTTGGAAAGACAGTTTGAGGAAGTTCCATTTAGGCCCTGGTATTTTGCAATGCGATTAAAGGAACTTTACAGATGCTGTGAAAGGTCTTTTACTAACGCGGCAAATAGAGGAA

>1635bp_PCR_prod lSEGUID
GCGCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGCAGCTGAAGCTTCGTACGCTGCAGGTCGACGGATCCCCGGGTTAATTAAGGCGCGCCAGATCTGTTTAGCTTGCCTCGTCCCCGCCGGGTCACCCGGCCAGCGACATGGAGGCCCAGAATACCCTCCTTGACAGTCTTGACGTGCGCAGCTCAGGGGCATGATGTGACTGTCGCCCGTACATTTAGCCCATACATCCCCATGTATAATCATTTGCATCCATACATTTTGATGGCCGCACGGCGCGAAGCAAAAATTACGGCTCCTCGCTGCAGACCTGCGAGCAGGGAAACGCTCCCCTCACAGACGCGTTGAATTGTCCCCACGCCGCGCCCCTGTAGAGAAATATAAAAGGTTAGGATTTGCCACTGAGGTTCTTCTTTCATATACTTCCTTTTAAAATCTTGCTAGGATACAGTTCTCACATCACATCCGAACATAAACAACCATGGGTAAGGAAAAGACTCACGTTTCGAGGCCGCGATTAAATTCCAACATGGATGCTGATTTATATGGGTATAAATGGGCTCGCGATAATGTCGGGCAATCAGGTGCGACAATCTATCGATTGTATGGGAAGCCCGATGCGCCAGAGTTGTTTCTGAAACATGGCAAAGGTAGCGTTGCCAATGATGTTACAGATGAGATGGTCAGACTAAACTGGCTGACGGAATTTATGCCTCTTCCGACCATCAAGCATTTTATCCGTACTCCTGATGATGCATGGTTACTCACCACTGCGATCCCCGGCAAAACAGCATTCCAGGTATTAGAAGAATATCCTGATTCAGGTGAAAATATTGTTGATGCGCTGGCAGTGTTCCTGCGCCGGTTGCATTCGATTCCTGTTTGTAATTGTCCTTTTAACAGCGATCGCGTATTTCGTCTCGCTCAGGCGCAATCACGAATGAATAACGGTTTGGTTGATGCGAGTGATTTTGATGACGAGCGTAATGGCTGGCCTGTTGAACAAGTCTGGAAAGAAATGCATAAGCTTTTGCCATTCTCACCGGATTCAGTCGTCACTCATGGTGATTTCTCACTTGATAACCTTATTTTTGACGAGGGGAAATTAATAGGTTGTATTGATGTTGGACGAGTCGGAATCGCAGACCGATACCAGGATCTTGCCATCCTATGGAACTGCCTCGGTGAGTTTTCTCCTTCATTACAGAAACGGCTTTTTCAAAAATATGGTATTGATAATCCTGATATGAATAAATTGCAGTTTCATTTGATGCTCGATGAGTTTTTCTAATCAGTACTGACAATAAAAAGATTCTTGTTTTCAAGAACTTGTCATTTGTATAGTTTTTTTATATTGTAGTTGTTCTATTTTAATCAAATGTTAGCGTGATTTATATTTTTTTTCGCCTCGACATCATCTGCCCAGATGCGAAGTTAAGTGCGCAGAAAGTAATATCATGCGTCAATCGTATGTGAATGCTGGTCGCTATACTGCTGTCGATTCGATACTAACGCCGCCATCCAGTGTCGAAAACGAGCTCGAATTCATCGATGATATCAGATCCACTAGTGGCCTATGCTGATTACGTTCTGCGATTTTCTCATGATCTTTTTCATAAAATACA

>ERG10_locus lSEGUID
ATTGAAGCACCTGTGGAGTATTTAAAAACTGCGGTTACATGGCCTACAGATGAAATATGTGCTCAACTAATGACACAATTCCCACCAGGAACGCCGACCAGTGTCCTGCTGCAGACTATTTCAGATGAGCTAGAGAAAAGTTCTGACAACCTGTTCACGTTATCTGATTTAAAGAGCAAACTGAAAGTTATTGGCTTATTCGAGCACATGGAAGATATCCCATTTTTCGACAAGCTGAAACTAAGCAATGCGCCCGTGAAGGACATGCCTATGGTCACAAAGGCGTTCACCAAATTTTGCGAAACAATAGCAAAAAGGCATACAAGAGGCCTACTGTCATACCGATTACCTTTTAACCTACTGGACTACAATTGCATACCGAATGAGAGTTATTCATTAGAGGTTTATGAGTCATTGTACAACATCATTACTCTATACTTCTGGCTCAGCAACAGGTACCCAAACTACTTCATTGACATGGAATCTGCTAAAGATTTGAAGTATTTCTGTGAGATGATTATTTTCGAGAAACTTGATCGATTAAAGAAGAATCCTTACGCACATAAGCCCTTTGGTTCTACAAGAGGTCACCTCTCATCTTCGAGAAGAAGATTGCGTACATAATCTACGATATATCCTGTAAATAGAAACAGCTACACTGCTTGAAAGCCTTAACATGATACATTTCTGGTATGATGCCATTGTTGTGCCCTGCCGGGTTTATCGTTTCCTAACAGGCACGTCACTTATAACGAGGTGCCTGTCGTTTACCGCCCAAGCCGGTTTTTTCGCTGGAGAGTACGGTACTACTAGCCCACCACACGTTCGTGGCCAGGTTGATAGGCCACCGTTGAGCAAAGGGCAGTAAAATATATAAAAGAGGAACAAGCGCTTCCATTAAGAGCACTGCTAAGCCTACTCGTTTTCTAGTTCTCTGAAAAAAGGTAGCCTAAAACAAGCGCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGTCTCAGAACGTTTACATTGTATCGACTGCCAGAACCCCAATTGGTTCATTCCAGGGTTCTCTATCCTCCAAGACAGCAGTGGAATTGGGTGCTGTTGCTTTAAAAGGCGCCTTGGCTAAGGTTCCAGAATTGGATGCATCCAAGGATTTTGACGAAATTATTTTTGGTAACGTTCTTTCTGCCAATTTGGGCCAAGCTCCGGCCAGACAAGTTGCTTTGGCTGCCGGTTTGAGTAATCATATCGTTGCAAGCACAGTTAACAAGGTCTGTGCATCCGCTATGAAGGCAATCATTTTGGGTGCTCAATCCATCAAATGTGGTAATGCTGATGTTGTCGTAGCTGGTGGTTGTGAATCTATGACTAACGCACCATACTACATGCCAGCAGCCCGTGCGGGTGCCAAATTTGGCCAAACTGTTCTTGTTGATGGTGTCGAAAGAGATGGGTTGAACGATGCGTACGATGGTCTAGCCATGGGTGTACACGCAGAAAAGTGTGCCCGTGATTGGGATATTACTAGAGAACAACAAGACAATTTTGCCATCGAATCCTACCAAAAATCTCAAAAATCTCAAAAGGAAGGTAAATTCGACAATGAAATTGTACCTGTTACCATTAAGGGATTTAGAGGTAAGCCTGATACTCAAGTCACGAAGGACGAGGAACCTGCTAGATTACACGTTGAAAAATTGAGATCTGCAAGGACTGTTTTCCAAAAAGAAAACGGTACTGTTACTGCCGCTAACGCTTCTCCAATCAACGATGGTGCTGCAGCCGTCATCTTGGTTTCCGAAAAAGTTTTGAAGGAAAAGAATTTGAAGCCTTTGGCTATTATCAAAGGTTGGGGTGAGGCCGCTCATCAACCAGCTGATTTTACATGGGCTCCATCTCTTGCAGTTCCAAAGGCTTTGAAACATGCTGGCATCGAAGACATCAATTCTGTTGATTACTTTGAATTCAATGAAGCCTTTTCGGTTGTCGGTTTGGTGAACACTAAGATTTTGAAGCTAGACCCATCTAAGGTTAATGTATATGGTGGTGCTGTTGCTCTAGGTCACCCATTGGGTTGTTCTGGTGCTAGAGTGGTTGTTACACTGCTATCCATCTTACAGCAAGAAGGAGGTAAGATCGGTGTTGCCGCCATTTGTAATGGTGGTGGTGGTGCTTCCTCTATTGTCATTGAAAAGATATGATTACGTTCTGCGATTTTCTCATGATCTTTTTCATAAAATACATAAATATATAAATGGCTTTATGTATAACAGGCATAATTTAAAGTTTTATTTGCGATTCATCGTTTTTCAGGTACTCAAACGCTGAGGTGTGCCTTTTGACTTACTTTTCCGCCTTGGCAAGCTGGCCGGGTGATACTTGCACAAGTTCCACTAATTACTGACATTTGTGGTATTAACTCGTTTGACTGCTCTACAATTGTAGGATGTTAATCAATGTCTTGGCTGCCTTCATTCTCTTCAGGCTCTATTAATTTTAACCGTTATAAGTTCCTTTTCTCCCTTGGAAGCAAACATCAACTGCCTTAAAATCTGGTGGCGAGGAAAGAGGAAATGGCATGTACTAATGATGGTCCTAATAAATATCCCGAAATTGTGAGTGTTAAGCACCTGTTCCAACATTCGGGATCCAAGCATGAATTTAGTGCTGGTAAACGATTTTCAAAATCCATTGGTAAAATATTCAAACGAAACTCTGCTTTGAAAACTTCTAGAACTGAAACGGCAAATCATAAAATGGAATTGAAAAAAAGAGAGGGTGTTACCTTATTGCCACCTGTCCCAGAATCATTATTACATAAACTCAATTCTTGGTTGGAAACTTTTTCTTCCACCAAGAACATGAAAATCGAAGAAAACAAAATTGTTATTAATGAAAAAGAGATTCGGGATTCAGTCTCTTACTACCCTGATAAGAATGGAGGAAGTGCTGTATTTTGTTACTTGCCCGACCTTGTGCTATATTATAAGCCGCCTATAAAAGTCACAGGCAAGCAATGTCCAATAAAGAGAAGTCCTTGGGAATCGATGGAAATCCAATATCAAAAGTTTATGTACCCCTTAGAAAGGTTGGAAAGACAGTTTGAGGAAGTTCCATTTAGGCCCTGGTATTTTGCAATGCGATTAAAGGAACTTTACAGATGCTGTGAAAGGTCTTTTACTAACGCGGCAAATAGAGGAA

>ERG10_locus_kanmx_ERG10_locus
ATTGAAGCACCTGTGGAGTATTTAAAAACTGCGGTTACATGGCCTACAGATGAAATATGT
GCTCAACTAATGACACAATTCCCACCAGGAACGCCGACCAGTGTCCTGCTGCAGACTATT
TCAGATGAGCTAGAGAAAAGTTCTGACAACCTGTTCACGTTATCTGATTTAAAGAGCAAA
CTGAAAGTTATTGGCTTATTCGAGCACATGGAAGATATCCCATTTTTCGACAAGCTGAAA
CTAAGCAATGCGCCCGTGAAGGACATGCCTATGGTCACAAAGGCGTTCACCAAATTTTGC
GAAACAATAGCAAAAAGGCATACAAGAGGCCTACTGTCATACCGATTACCTTTTAACCTA
CTGGACTACAATTGCATACCGAATGAGAGTTATTCATTAGAGGTTTATGAGTCATTGTAC
AACATCATTACTCTATACTTCTGGCTCAGCAACAGGTACCCAAACTACTTCATTGACATG
GAATCTGCTAAAGATTTGAAGTATTTCTGTGAGATGATTATTTTCGAGAAACTTGATCGA
TTAAAGAAGAATCCTTACGCACATAAGCCCTTTGGTTCTACAAGAGGTCACCTCTCATCT
TCGAGAAGAAGATTGCGTACATAATCTACGATATATCCTGTAAATAGAAACAGCTACACT
GCTTGAAAGCCTTAACATGATACATTTCTGGTATGATGCCATTGTTGTGCCCTGCCGGGT
TTATCGTTTCCTAACAGGCACGTCACTTATAACGAGGTGCCTGTCGTTTACCGCCCAAGC
CGGTTTTTTCGCTGGAGAGTACGGTACTACTAGCCCACCACACGTTCGTGGCCAGGTTGA
TAGGCCACCGTTGAGCAAAGGGCAGTAAAATATATAAAAGAGGAACAAGCGCTTCCATTA
AGAGCACTGCTAAGCCTACTCGTTTTCTAGTTCTCTGAAAAAAGGTAGCCTAAAACAAGC
GCCATATCATATATATTTATACAGATTAGACGTACTCAAAATGCAGCTGAAGCTTCGTAC
GCTGCAGGTCGACGGATCCCCGGGTTAATTAAGGCGCGCCAGATCTGTTTAGCTTGCCTC
GTCCCCGCCGGGTCACCCGGCCAGCGACATGGAGGCCCAGAATACCCTCCTTGACAGTCT
TGACGTGCGCAGCTCAGGGGCATGATGTGACTGTCGCCCGTACATTTAGCCCATACATCC
CCATGTATAATCATTTGCATCCATACATTTTGATGGCCGCACGGCGCGAAGCAAAAATTA
CGGCTCCTCGCTGCAGACCTGCGAGCAGGGAAACGCTCCCCTCACAGACGCGTTGAATTG
TCCCCACGCCGCGCCCCTGTAGAGAAATATAAAAGGTTAGGATTTGCCACTGAGGTTCTT
CTTTCATATACTTCCTTTTAAAATCTTGCTAGGATACAGTTCTCACATCACATCCGAACA
TAAACAACCATGGGTAAGGAAAAGACTCACGTTTCGAGGCCGCGATTAAATTCCAACATG
GATGCTGATTTATATGGGTATAAATGGGCTCGCGATAATGTCGGGCAATCAGGTGCGACA
ATCTATCGATTGTATGGGAAGCCCGATGCGCCAGAGTTGTTTCTGAAACATGGCAAAGGT
AGCGTTGCCAATGATGTTACAGATGAGATGGTCAGACTAAACTGGCTGACGGAATTTATG
CCTCTTCCGACCATCAAGCATTTTATCCGTACTCCTGATGATGCATGGTTACTCACCACT
GCGATCCCCGGCAAAACAGCATTCCAGGTATTAGAAGAATATCCTGATTCAGGTGAAAAT
ATTGTTGATGCGCTGGCAGTGTTCCTGCGCCGGTTGCATTCGATTCCTGTTTGTAATTGT
CCTTTTAACAGCGATCGCGTATTTCGTCTCGCTCAGGCGCAATCACGAATGAATAACGGT
TTGGTTGATGCGAGTGATTTTGATGACGAGCGTAATGGCTGGCCTGTTGAACAAGTCTGG
AAAGAAATGCATAAGCTTTTGCCATTCTCACCGGATTCAGTCGTCACTCATGGTGATTTC
TCACTTGATAACCTTATTTTTGACGAGGGGAAATTAATAGGTTGTATTGATGTTGGACGA
GTCGGAATCGCAGACCGATACCAGGATCTTGCCATCCTATGGAACTGCCTCGGTGAGTTT
TCTCCTTCATTACAGAAACGGCTTTTTCAAAAATATGGTATTGATAATCCTGATATGAAT
AAATTGCAGTTTCATTTGATGCTCGATGAGTTTTTCTAATCAGTACTGACAATAAAAAGA
TTCTTGTTTTCAAGAACTTGTCATTTGTATAGTTTTTTTATATTGTAGTTGTTCTATTTT
AATCAAATGTTAGCGTGATTTATATTTTTTTTCGCCTCGACATCATCTGCCCAGATGCGA
AGTTAAGTGCGCAGAAAGTAATATCATGCGTCAATCGTATGTGAATGCTGGTCGCTATAC
TGCTGTCGATTCGATACTAACGCCGCCATCCAGTGTCGAAAACGAGCTCGAATTCATCGA
TGATATCAGATCCACTAGTGGCCTATGCTGATTACGTTCTGCGATTTTCTCATGATCTTT
TTCATAAAATACATAAATATATAAATGGCTTTATGTATAACAGGCATAATTTAAAGTTTT
ATTTGCGATTCATCGTTTTTCAGGTACTCAAACGCTGAGGTGTGCCTTTTGACTTACTTT
TCCGCCTTGGCAAGCTGGCCGGGTGATACTTGCACAAGTTCCACTAATTACTGACATTTG
TGGTATTAACTCGTTTGACTGCTCTACAATTGTAGGATGTTAATCAATGTCTTGGCTGCC
TTCATTCTCTTCAGGCTCTATTAATTTTAACCGTTATAAGTTCCTTTTCTCCCTTGGAAG
CAAACATCAACTGCCTTAAAATCTGGTGGCGAGGAAAGAGGAAATGGCATGTACTAATGA
TGGTCCTAATAAATATCCCGAAATTGTGAGTGTTAAGCACCTGTTCCAACATTCGGGATC
CAAGCATGAATTTAGTGCTGGTAAACGATTTTCAAAATCCATTGGTAAAATATTCAAACG
AAACTCTGCTTTGAAAACTTCTAGAACTGAAACGGCAAATCATAAAATGGAATTGAAAAA
AAGAGAGGGTGTTACCTTATTGCCACCTGTCCCAGAATCATTATTACATAAACTCAATTC
TTGGTTGGAAACTTTTTCTTCCACCAAGAACATGAAAATCGAAGAAAACAAAATTGTTAT
TAATGAAAAAGAGATTCGGGATTCAGTCTCTTACTACCCTGATAAGAATGGAGGAAGTGC
TGTATTTTGTTACTTGCCCGACCTTGTGCTATATTATAAGCCGCCTATAAAAGTCACAGG
CAAGCAATGTCCAATAAAGAGAAGTCCTTGGGAATCGATGGAAATCCAATATCAAAAGTT
TATGTACCCCTTAGAAAGGTTGGAAAGACAGTTTGAGGAAGTTCCATTTAGGCCCTGGTA
TTTTGCAATGCGATTAAAGGAACTTTACAGATGCTGTGAAAGGTCTTTTACTAACGCGGC
AAATAGAGGAA
```

### crispr

```
# crispr

This snippet describe a CRISPr digestion and recombination

>guide sgRNA construct containing a scaffold sequence
gatc....

>target DNA to be cut (linear *or* circular)
gatc...

>sequence1 a result from digestion of target (linear)
gatc...

>sequence2 another result from digestion of target (linear)
actg...

...
```



## More examples

A lactose metabolic [pathway](https://github.com/MetabolicEngineeringGroupCBMA/Lactose-Pathway) for *S. cerevisiae* was formulated using this method. The pathway contains two expression cassettes with the Kluyveromyces lactis beta-D-galactosidase `LAC4` and  the `LAC12` Kluyveromyces lactis LAC12 gene for lactose permease. You can download the files by using the `Code` button and then the `Download ZIP` button:

![[dlzip.png]]

Briefly:

1. LAC4 was pcr amplified from chromosomal DNA.
2. The PCR product was cloned in the pYPKa vector in the *Aji*I site.
3. A DNA fragment was pcr amplified from the pYPKa_A_LAC4 vector
4. A promoter was amplified from the pYPKa_Z_PDC1 plasmid
5. A terminator was amplified from the pYPKa_E_PGI1 plasmid
6. The promoter gene and terminator and the vector pYPKpw digested with *Zra*I was joined by recombination to form the `pYPK0_PDC1_KlLAC4_PGI1` circular plasmid.

The same procedure was performed for the LAC12 but with the `pYPKa_Z_PGI1` vector for the promoter and `pYPKa_E_TPI1` for terminator. The resulting vector is called `pYPK0_PGI1_KlLAC12_TPI1`.

The two expression cassettes were pcr amplified and joined by homologous recombination with a pYPKpw vector digested with *Zra*I resulting in the
`pYPK0_PDC1_KlLAC4_PGI1_KlLAC12_TPI1` vector expressing both genes.

In this example, each file contain only one snippet, but all snippets could be put in one file.

The advantage of separate files is that they can be reused.

Each file name starts with the header of the snippet, like "pcr_...".
This is optional, but makes it easier to sort the files.
