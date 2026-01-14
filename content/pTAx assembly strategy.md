pTA vectors are built from five PCR products (Figure 1).

This [table](https://docs.google.com/spreadsheets/d/1KV2RtKb4NI7cfrAcmUzHkosKOWJPmzKwOHyGJeM2HlE/edit?usp=sharing) contain primer numbers and template plasmids for each of the five PCR products for all current pTAx vectors. Each PCR reaction is marked with a different color.

All further information needed to assemble a pTAx vector *in-silico* is available on this page. Table 1 contain plasmid sequences and Table 2 all primer sequences.

The plasmids can be assembled using the [Pydnaweb](https://pydnaweb.streamlit.app/) PCR and  assembly simulators.

#### Figure 1
![[tailed_pcr_products.png]]

The PCR products are made with primers that incorporate five different specific flanking sequences on each end of the PCR products, (❶..❺) in Figure 1. The extra sequence introduced by adding nucleotides to the 5' part of the primer that do not anneal to the template (a primer tail). These are indicated in Figure 2.

#### Figure 2
![[tailed_primer_pcr.png]]


These flanking sequences will enable homologous recombination between the DNA fragments in a specific order. The vectors are assembled by homologous recombination between the❶..❺ sequences as shown in Figure 3.
#### Figure 3
![[pTA_vectors.png]]



#### Table 1 Plasmid links

Links to sequences and references for each source plasmid.

| Table 1 | Plasmid              | Freezer#         | Reference                                                                                                          | Genbank (Gb)                                                               | Snapgene (Sg)                                                                   | Gb vs. Sg                                     | 👌 Recommended sequence                                                                                                                  | seguid                               |
| ------- | -------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
|         | pBR322               | µ831             | [link](https://pubmed.ncbi.nlm.nih.gov/344137)                                                                     | [J01749](https://www.ncbi.nlm.nih.gov/nuccore/J01749.1)                    | [link](https://www.snapgene.com/plasmids/basic_cloning_vectors/pBR322)          | Same size; 1 nt missense in Tc gene.          | Genbank                                                                                                                                  | cdseguid=H-FY2ZzvKeazrRW2dNeSeMikjoc |
|         | pTA1                 | µ828, µ928, µ929 | [link](https://www.sciencedirect.com/science/article/pii/S221403012300007X)                                        | -                                                                          | -                                                                               |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/YeastPathwayKit/blob/master/sequences/pTA1.gb)                                 | cdseguid=MtltqcR0b0kVX_FJ4BYL-PjEAfg |
|         | pYPKpw               | µ463             | [link](https://github.com/MetabolicEngineeringGroupCBMA/ypk-xylose-pathways?tab=readme-ov-file#pereira-et-al-2016) | -                                                                          | -                                                                               |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/YeastPathwayKit/blob/master/sequences/pYPKpw.gb)                               | cdseguid=xj7evEO4h83-RGFeHu8q15tL_Qs |
|         | p423GPD              | µ601             | [link](https://www.sciencedirect.com/science/article/pii/0378111995000377?via%3Dihub)                              | -                                                                          | -                                                                               |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/pydna-examples/blob/master/notebooks/mumberg_32_expression_vectors/p423GPD.gb) |                                      |
|         | pFA6a-GFPS65T-kanMX6 | µ716             | [link](https://onlinelibrary.wiley.com/doi/10.1002/(SICI)1097-0061(19970915)13:11%3C1065::AID-YEA159%3E3.0.CO;2-K) | [AJ002682.1](https://www.ncbi.nlm.nih.gov/nucleotide/AJ002682.1)           | [link](https://www.snapgene.com/plasmids/yeast_plasmids/pFA6a-GFP(S65T)-kanMX6) |                                               |                                                                                                                                          | cdseguid=fisQRzPkD-XD07m2YQFOa2B1NdA |
|         | pSH65                | µ853             | [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC101367)                                                        | [AF298780.1](https://www.ncbi.nlm.nih.gov/nucleotide/AF298780.1) (partial) | -                                                                               | Gb has a1 nt insertion.                       | [EUROSCARF](http://www.euroscarf.de/plasmid_details.php?accno=P30122) (complete)                                                         |                                      |
|         | pUG35                | µ762             | -                                                                                                                  | [AF298787.1](https://www.ncbi.nlm.nih.gov/nucleotide/AF298787.1)           | -                                                                               |                                               |                                                                                                                                          |                                      |
|         | YEplac112            | µ661             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75458.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75458.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YEplac112)              | 1 snp in pUC origin                           | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YEplac112_snapgene.gb)                              | cdseguid=MLKxSGFkZsuuiqozB87sVQQ0xaU |
|         | YEplac195            | µ662             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75459.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75459.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YEplac195)              | 1 snp in pUC origin                           | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YEplac195_snapgene.gb)                              | cdseguid=nsxZh92qaUyjufyG0goiB3-Aq8c |
|         | YEplac181            | µ663             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75460.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75460.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YEplac181)              | 12 bp deletion in end of LEU2 promoter in Gb. | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YEplac181_snapgene.gb)                              | cdseguid=gZjQlzVQtwNzfV1XOFu1psiO2Eo |
|         | YIplac204            | µ664             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75461.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75461.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YIplac204)              | 1 snp in pUC origin                           | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YIplac204_snapgene.gb)                              | cdseguid=24fcVzVrHWTQXwerHr3_OyEw9D0 |
|         | YIplac211            | µ665             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75462.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75462.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YIplac211)              | 1 snp in pUC origin                           | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YIplac211_snapgene.gb)                              | cdseguid=U-L4v2SU5qf0bIra0ANlXaGVXlM |
|         | YIplac128            | µ666             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75463.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75463.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YIplac128)              | Deletion in start of LEU2 for Gb              | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YIplac128_snapgene.gb)                              | cdseguid=Ch6Y7zxAoVN5PAGDHKdzT2AFmm8 |
|         | YCplac22             | µ658             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75455.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75455.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YCplac22)               |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YCplac22_snapgene.gb)<br>                           | cdseguid=BB-iNIXT2u55EuDhEHH0yufrGWg |
|         | YCplac33             | µ659             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75456.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75456.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YCplac33)               |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YCplac33_snapgene.gb)<br>                           | cdseguid=XyTO5X31FUQgGt9m4roqPDTDzZs |
|         | YCplac111            | µ660             | [link](https://pubmed.ncbi.nlm.nih.gov/3073106/)                                                                   | [X75457.1](https://www.ncbi.nlm.nih.gov/nucleotide/X75457.1)               | [link](https://www.snapgene.com/plasmids/yeast_plasmids/YCplac111)              |                                               | [GitHub](https://github.com/MetabolicEngineeringGroupCBMA/public-sequences/blob/main/YCplac111_snapgene.gb)                              | cdseguid=7ytS0ma8bAjM9lEcozGnQDYtse8 |


#### Table 2 Primer sequences
```
>1750_s1 s1 tm=52.856
AATCCAATCAGCGTAAG

>1749_s2 s2 tm=56.264
ATCGTATCTGCTGCGT

>1748_s3 s3 tm=53.243
TAAAATCTCGTAAAGGAACT

>1747_s4 s4 tm=52.983
AACTGTAAAATCAGGTATCT

>1746_s5 s5 tm=54.852
GAAAAGCGTTTACCTCG

>1745_s1r s1r tm=52.348
AGAAAGTCTACACCTTAC

>1744_s2r s2r tm=54.01
GTTGACTACTATTTACGCA

>1743_s3r s3r tm=55.045
CAGAGCAGACAGTTCC

>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC

>1741_s5r s5r tm=51.462
TACAATAGAGTTCCGAG

>1222_2954fw 29-mer
GAAATTTCAGCCACTTCACAGGCGGTTTT

>1779_pUCmu_bb_R 24-mer
actcttcctttttcaatattattg

>1804_TRP1fp_pTA replaces 1348 & 1680
TAAAATCTCGTAAAGGAACTGTCTGCTCTGtataaaaataggcgtatcacg

>1691_URA3fp_pTA_2
TAAAATCTCGTAAAGGAACTGTCTGCTCTGgcttttcaattcaattcatc

>1690_HIS3rp_pTA_2
ACGGACTACGAGATACCTGATTTTACAGTTgacacgtatagaatgatg

>1681_Pbr.FW.2 New pBR primer, partial s1, replaces 1196
TAAGGTGTAGACTTTCTccgtagaaaagatcaaag

>1680_TRP1fp_pTA New TRP1 primer, partial s3, replaces 1348, replaced by 1804
GAACTGTCTGCTCTGttcaagaattaattcggtcg

>1352_HIS3fp_pTA
TAAAATCTCGTAAAGGAACTGTCTGCTCTGAACACAGTCCTTTCC

>1351_HIS3rp_pTA
ACGGACTACGAGATACCTGATTTTACAGTTTTTTTTCTCGAGTTCAAGA

>1350_KanMX4fp_pTA
TAAAATCTCGTAAAGGAACTGTCTGCTCTGGACATGGAGGCCC

>1349_KanMX4rp_pTA
ACGGACTACGAGATACCTGATTTTACAGTTCAGTATAGCGACCAGC

>1348_TRP1fp_pTA
TAAAATCTCGTAAAGGAACTGTCTGCTCTGTTTGCCGATTAAGAATTCG

>1347_TRP1rp_pTA
ACGGACTACGAGATACCTGATTTTACAGTTGATCTTTTATGCTTGCTTTTC

>1346_URA3fp_pTA
TAAAATCTCGTAAAGGAACTGTCTGCTCTGGATTCCGGTTTCTTTGAAA

>1345_URA3rp_pTA
ACGGACTACGAGATACCTGATTTTACAGTTGGTAATAACTGATATAATTAAATTGAA

>1344_CEN_ARSfp_pTA
ATCGTATCTGCTGCGTAAATAGTAGTCAACACGGATCGCTTGC

>1343_CEN_ARSrp_pTA
CAGAGCAGACAGTTCCTTTACGAGATTTTACTTTTCATCACGTGCTATA

>1196_Pbr.FW
AATCCAATCAGCGTAAGGTGTAGACTTTCTCTGTCAGACCAAGTTTACT

>1195_Pbr.REV
GTTGACTACTATTTACGCAGCAGATACGATCTCGTTTCATCGGT

>1113_Amp.fw.nw
GAAAAGCGTTTACCTCGGAACTCTATTGTAGAACCCCTATTTGTTTATTTTTCTA

>988_Amp.FW Amp.FW (do not use!)
GAAAAGCGTTTACCTCGGAACTCTATTGTAAACCCTGATAAATGCTTC

>987_Amp.REV Amp.REV
AGAAAGTCTACACCTTACGCTGATTGGATTTGAAGTTTTAAATCAATCTAAA

>986_Pbr.FW Pbr.FW
AATCCAATCAGCGTAAGGTGTAGACTTTCTCTCGTTTCATCGGTAT

>985_Pbr.REV Pbr.REV
GTTGACTACTATTTACGCAGCAGATACGATCTGTCAGACCAAGTTTACT

>984_Micron.FW Micron.FW
ATCGTATCTGCTGCGTAAATAGTAGTCAACGATCGTACTTGTTACCCAT

>983_Micron.REV Micron.REV
CAGAGCAGACAGTTCCTTTACGAGATTTTAGATCCAATATCAAAGGAA

>982_dLeu.FW dLeu.FW
TAAAATCTCGTAAAGGAACTGTCTGCTCTTATATATATTTCAAGGATATACCATT

>981_dLeu.REV dLeu.REV
ACGGACTACGAGATACCTGATTTTACAGTTTAAGGCCGTTTCTGAC

>980_Leu2.FW Leu2.FW
TAAAATCTCGTAAAGGAACTGTCTGCTCTGTTAACTGTGGGAATACTC

>979_Leu2.REV Leu2.REV
ACGGACTACGAGATACCTGATTTTACAGTTTCTACCCTATGAACATATTC

>978_Crp.FW Crp.FW
AACTGTAAAATCAGGTATCTCGTAGTCCGTGTTCTGATCCTCGAGC

>977_Crp.REV Crp.REV
TACAATAGAGTTCCGAGGTAAACGCTTTTCGTTCTTGTCTCATTGCC

```

| Table 3 | Icon | Designation | Recombination sequence (30 bp)   |
| ------- | ---- | ----------- | -------------------------------- |
|         | ❶    | s1          | `AATCCAATCAGCGTAAGGTGTAGACTTTCT` |
|         | ❷    | s2          | `ATCGTATCTGCTGCGTAAATAGTAGTCAAC` |
|         | ❸    | s3          | `TAAAATCTCGTAAAGGAACTGTCTGCTCTG` |
|         | ❹    | s4          | `AACTGTAAAATCAGGTATCTCGTAGTCCGT` |
|         | ❺    | s5          | `GAAAAGCGTTTACCTCGGAACTCTATTGTA` |
|         | ❻    | s6          | `TTTACCTGTGGATTGATAGGAATACACCCA` |
Designed with the [R2oDNA designer](https://pubmed.ncbi.nlm.nih.gov/24933158) tool.