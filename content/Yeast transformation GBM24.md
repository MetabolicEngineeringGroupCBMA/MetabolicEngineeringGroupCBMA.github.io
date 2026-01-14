# Yeast transformation and *In-vivo* plasmid assembly

![[Yeast transformation GBM24-20240924183141411.png]]

The aim of this practical class is to transform yeast carrying a circular plasmid `pTA1_TDH3_ScATF1_PGI1` with a PCR product containing the [[kanMX4]] selectable marker. The PCR product contain flanking sequences by which in can recombine with the plasmid *in-vivo*.

![[Yeast transformation GBM24-20240930112004211.png]]

The expected result would be a plasmid where the KanMX4  geneticin resistance marker will replace the LEU2 marker in the final plasmid. This will happen through homologous recombination between a circular and a linear DNA molecule.

We can obtain the KanMX DNA fragment by PCR using the primers 1350 and 1349 the pUG6 plasmid.

```
>1350_KanMX4fp_pTA
TAAAATCTCGTAAAGGAACTGTCTGCTCTGGACATGGAGGCCC

>1349_KanMX4rp_pTA
ACGGACTACGAGATACCTGATTTTACAGTTCAGTATAGCGACCAGC

>AF298793.1 PCR template vector pUG6, complete sequence circular
GAACGCGGCCGCCAGCTGAAGCTTCGTACGCTGCAGGTCGACAACCCTTAATATAACTTCGTATAATGTATGCTATACGAAGTTATTAGGTCTAGAGATCTGTTTAGCTTGCCTCGTCCCCGCCGGGTCACCCGGCCAGCGACATGGAGGCCCAGAATACCCTCCTTGACAGTCTTGACGTGCGCAGCTCAGGGGCATGATGTGACTGTCGCCCGTACATTTAGCCCATACATCCCCATGTATAATCATTTGCATCCATACATTTTGATGGCCGCACGGCGCGAAGCAAAAATTACGGCTCCTCGCTGCAGACCTGCGAGCAGGGAAACGCTCCCCTCACAGACGCGTTGAATTGTCCCCACGCCGCGCCCCTGTAGAGAAATATAAAAGGTTAGGATTTGCCACTGAGGTTCTTCTTTCATATACTTCCTTTTAAAATCTTGCTAGGATACAGTTCTCACATCACATCCGAACATAAACAACCATGGGTAAGGAAAAGACTCACGTTTCGAGGCCGCGATTAAATTCCAACATGGATGCTGATTTATATGGGTATAAATGGGCTCGCGATAATGTCGGGCAATCAGGTGCGACAATCTATCGATTGTATGGGAAGCCCGATGCGCCAGAGTTGTTTCTGAAACATGGCAAAGGTAGCGTTGCCAATGATGTTACAGATGAGATGGTCAGACTAAACTGGCTGACGGAATTTATGCCTCTTCCGACCATCAAGCATTTTATCCGTACTCCTGATGATGCATGGTTACTCACCACTGCGATCCCCGGCAAAACAGCATTCCAGGTATTAGAAGAATATCCTGATTCAGGTGAAAATATTGTTGATGCGCTGGCAGTGTTCCTGCGCCGGTTGCATTCGATTCCTGTTTGTAATTGTCCTTTTAACAGCGATCGCGTATTTCGTCTCGCTCAGGCGCAATCACGAATGAATAACGGTTTGGTTGATGCGAGTGATTTTGATGACGAGCGTAATGGCTGGCCTGTTGAACAAGTCTGGAAAGAAATGCATAAGCTTTTGCCATTCTCACCGGATTCAGTCGTCACTCATGGTGATTTCTCACTTGATAACCTTATTTTTGACGAGGGGAAATTAATAGGTTGTATTGATGTTGGACGAGTCGGAATCGCAGACCGATACCAGGATCTTGCCATCCTATGGAACTGCCTCGGTGAGTTTTCTCCTTCATTACAGAAACGGCTTTTTCAAAAATATGGTATTGATAATCCTGATATGAATAAATTGCAGTTTCATTTGATGCTCGATGAGTTTTTCTAATCAGTACTGACAATAAAAAGATTCTTGTTTTCAAGAACTTGTCATTTGTATAGTTTTTTTATATTGTAGTTGTTCTATTTTAATCAAATGTTAGCGTGATTTATATTTTTTTTCGCCTCGACATCATCTGCCCAGATGCGAAGTTAAGTGCGCAGAAAGTAATATCATGCGTCAATCGTATGTGAATGCTGGTCGCTATACTGCTGTCGATTCGATACTAACGCCGCCATCCAGTGTCGAAAACGAGCTCTCGAGAACCCTTAATATAACTTCGTATAATGTATGCTATACGAAGTTATTAGGTGATATCAGATCCACTAGTGGCCTATGCGGCCGCGGATCTGCCGGTCTCCCTATAGTGAGTCGTATTAATTTCGATAAGCCAGGTTAACCTGCATTAATGAATCGGCCAACGCGCGGGGAGAGGCGGTTTGCGTATTGGGCGCTCTTCCGCTTCCTCGCTCACTGACTCGCTGCGCTCGGTCGTTCGGCTGCGGCGAGCGGTATCAGCTCACTCAAAGGCGGTAATACGGTTATCCACAGAATCAGGGGATAACGCAGGAAAGAACATGTGAGCAAAAGGCCAGCAAAAGGCCAGGAACCGTAAAAAGGCCGCGTTGCTGGCGTTTTTCCATAGGCTCCGCCCCCCTGACGAGCATCACAAAAATCGACGCTCAAGTCAGAGGTGGCGAAACCCGACAGGACTATAAAGATACCAGGCGTTTCCCCCTGGAAGCTCCCTCGTGCGCTCTCCTGTTCCGACCCTGCCGCTTACCGGATACCTGTCCGCCTTTCTCCCTTCGGGAAGCGTGGCGCTTTCTCAATGCTCACGCTGTAGGTATCTCAGTTCGGTGTAGGTCGTTCGCTCCAAGCTGGGCTGTGTGCACGAACCCCCCGTTCAGCCCGACCGCTGCGCCTTATCCGGTAACTATCGTCTTGAGTCCAACCCGGTAAGACACGACTTATCGCCACTGGCAGCAGCCACTGGTAACAGGATTAGCAGAGCGAGGTATGTAGGCGGTGCTACAGAGTTCTTGAAGTGGTGGCCTAACTACGGCTACACTAGAAGGACAGTATTTGGTATCTGCGCTCTGCTGAAGCCAGTTACCTTCGGAAAAAGAGTTGGTAGCTCTTGATCCGGCAAACAAACCACCGCTGGTAGCGGTGGTTTTTTTGTTTGCAAGCAGCAGATTACGCGCAGAAAAAAAGGATCTCAAGAAGATCCTTTGATCTTTTCTACGGGGTCTGACGCTCAGTGGAACGAAAACTCACGTTAAGGGATTTTGGTCATGAGATTATCAAAAAGGATCTTCACCTAGATCCTTTTAAATTAAAAATGAAGTTTTAAATCAATCTAAAGTATATATGAGTAAACTTGGTCTGACAGTTACCAATGCTTAATCAGTGAGGCACCTATCTCAGCGATCTGTCTATTTCGTTCATCCATAGTTGCCTGACTCCCCGTCGTGTAGATAACTACGATACGGGAGGGCTTACCATCTGGCCCCAGTGCTGCAATGATACCGCGAGACCCACGCTCACCGGCTCCAGATTTATCAGCAATAAACCAGCCAGCCGGAAGGGCCGAGCGCAGAAGTGGTCCTGCAACTTTATCCGCCTCCATCCAGTCTATTAATTGTTGCCGGGAAGCTAGAGTAAGTAGTTCGCCAGTTAATAGTTTGCGCAACGTTGTTGCCATTGCTACAGGCATCGTGGTGTCACGCTCGTCGTTTGGTATGGCTTCATTCAGCTCCGGTTCCCAACGATCAAGGCGAGTTACATGATCCCCCATGTTGTGCAAAAAAGCGGTTAGCTCCTTCGGTCCTCCGATCGTTGTCAGAAGTAAGTTGGCCGCAGTGTTATCACTCATGGTTATGGCAGCACTGCATAATTCTCTTACTGTCATGCCATCCGTAAGATGCTTTTCTGTGACTGGTGAGTACTCAACCAAGTCATTCTGAGAATAGTGTATGCGGCGACCGAGTTGCTCTTGCCCGGCGTCAATACGGGATAATACCGCGCCACATAGCAGAACTTTAAAAGTGCTCATCATTGGAAAACGTTCTTCGGGGCGAAAACTCTCAAGGATCTTACCGCTGTTGAGATCCAGTTCGATGTAACCCACTCGTGCACCCAACTGATCTTCAGCATCTTTTACTTTCACCAGCGTTTCTGGGTGAGCAAAAACAGGAAGGCAAAATGCCGCAAAAAAGGGAATAAGGGCGACACGGAAATGTTGAATACTCATACTCTTCCTTTTTCAATATTATTGAAGCATTTATCAGGGTTATTGTCTCATGAGCGGATACATATTTGAATGTATTTAGAAAAATAAACAAATAGGGGTTCCGCGCACATTTCCCCGAAAAGTGCCACCTGACGTCTAAGAAACCATTATTATCATGACATTAACCTATAAAAATAGGCGTATCACGAGGCCCTTTCGTCTCGCGCGTTTCGGTGATGACGGTGAAAACCTCTGACACATGCAGCTCCCGGAGACGGTCACAGCTTGTCTGTAAGCGGATGCCGGGAGCAGACAAGCCCGTCAGGGCGCGTCAGCGGGTGTTGGCGGGTGTCGGGGCTGGCTTAACTATGCGGCATCAGAGCAGATTGTACTGAGAGTGCACCATATGGACATATTGTCGTTAGAACGCGGCTACAATTAATACATAACCTTATGTATCATACACATACGATTTAGGTGACACTATA

Template AF298793.1 4009 bp circular limit=12:
1350_KanMX4fp_pTA anneals forward (--->) at 13
1349_KanMX4rp_pTA anneals reverse (<---) at 1341
---
Forward: 1350_KanMX4fp_pTA Reverse: 1349_KanMX4rp_pTA

                              5GACATGGAGGCCC...GCTGGTCGCTATACTG3
                                               ||||||||||||||||
                                              3CGACCAGCGATATGACTTGACATTTTAGTCCATAGAGCATCAGGCA5
5TAAAATCTCGTAAAGGAACTGTCTGCTCTGGACATGGAGGCCC3
                               |||||||||||||
                              3CTGTACCTCCGGG...CGACCAGCGATATGAC5

Taq DNA pol
|95°C|95°C               |    |tmf:52.2
|____|_____          72°C|72°C|tmr:54.1
|3min|30s  \ 54.8°C _____|____|45s/kb
|    |      \______/ 1:03|5min|GC 43%
|    |       30s         |    |1417bp


>1417bp_PCR_prod
TAAAATCTCGTAAAGGAACTGTCTGCTCTGGACATGGAGGCCCAGAATACCCTCCTTGACAGTCTTGACGTGCGCAGCTCAGGGGCATGATGTGACTGTCGCCCGTACATTTAGCCCATACATCCCCATGTATAATCATTTGCATCCATACATTTTGATGGCCGCACGGCGCGAAGCAAAAATTACGGCTCCTCGCTGCAGACCTGCGAGCAGGGAAACGCTCCCCTCACAGACGCGTTGAATTGTCCCCACGCCGCGCCCCTGTAGAGAAATATAAAAGGTTAGGATTTGCCACTGAGGTTCTTCTTTCATATACTTCCTTTTAAAATCTTGCTAGGATACAGTTCTCACATCACATCCGAACATAAACAACCATGGGTAAGGAAAAGACTCACGTTTCGAGGCCGCGATTAAATTCCAACATGGATGCTGATTTATATGGGTATAAATGGGCTCGCGATAATGTCGGGCAATCAGGTGCGACAATCTATCGATTGTATGGGAAGCCCGATGCGCCAGAGTTGTTTCTGAAACATGGCAAAGGTAGCGTTGCCAATGATGTTACAGATGAGATGGTCAGACTAAACTGGCTGACGGAATTTATGCCTCTTCCGACCATCAAGCATTTTATCCGTACTCCTGATGATGCATGGTTACTCACCACTGCGATCCCCGGCAAAACAGCATTCCAGGTATTAGAAGAATATCCTGATTCAGGTGAAAATATTGTTGATGCGCTGGCAGTGTTCCTGCGCCGGTTGCATTCGATTCCTGTTTGTAATTGTCCTTTTAACAGCGATCGCGTATTTCGTCTCGCTCAGGCGCAATCACGAATGAATAACGGTTTGGTTGATGCGAGTGATTTTGATGACGAGCGTAATGGCTGGCCTGTTGAACAAGTCTGGAAAGAAATGCATAAGCTTTTGCCATTCTCACCGGATTCAGTCGTCACTCATGGTGATTTCTCACTTGATAACCTTATTTTTGACGAGGGGAAATTAATAGGTTGTATTGATGTTGGACGAGTCGGAATCGCAGACCGATACCAGGATCTTGCCATCCTATGGAACTGCCTCGGTGAGTTTTCTCCTTCATTACAGAAACGGCTTTTTCAAAAATATGGTATTGATAATCCTGATATGAATAAATTGCAGTTTCATTTGATGCTCGATGAGTTTTTCTAATCAGTACTGACAATAAAAAGATTCTTGTTTTCAAGAACTTGTCATTTGTATAGTTTTTTTATATTGTAGTTGTTCTATTTTAATCAAATGTTAGCGTGATTTATATTTTTTTTCGCCTCGACATCATCTGCCCAGATGCGAAGTTAAGTGCGCAGAAAGTAATATCATGCGTCAATCGTATGTGAATGCTGGTCGCTATACTGAACTGTAAAATCAGGTATCTCGTAGTCCGT
---

```

We can obtain the KanMX DNA fragment by PCR using the primers 1748 and 1742 the pTA5 plasmid.


```
>1748_s3 s3 tm=53.243
TAAAATCTCGTAAAGGAACT

>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC

>pTA5 circular
tcgcgcgtttcggtgatgacggtgaaaacctctgacacatgcagctcccggagacggtcacagcttgtctgtaagcggatgccgggagcagacaagcccgtcagggcgcgtcagcgggtgttggcgggtgtcggggcgcagccatgacccagtcacgtagcgatagcggagtgtatactggcttaactatgcggcatcagagcagattgtactgagagtgcaccatatgcggtgtgaaataccgcacagatgcgtaaggagaaaataccgcatcaggcgctcttccgcttcctcgctcactgactcgctgcgctcggtcgttcggctgcggcgagcggtatcagctcactcaaaggcggtaatacggttatccacagaatcaggggataacgcaggaaagaacatgtgagcaaaaggccagcaaaaggccaggaaccgtaaaaaggccgcgttgctggcgtttttccataggctccgcccccctgacgagcatcacaaaaatcgacgctcaagtcagaggtggcgaaacccgacaggactataaagataccaggcgtttccccctggaagctccctcgtgcgctctcctgttccgaccctgccgcttaccggatacctgtccgcctttctcccttcgggaagcgtggcgctttctcatagctcacgctgtaggtatctcagttcggtgtaggtcgttcgctccaagctgggctgtgtgcacgaaccccccgttcagcccgaccgctgcgccttatccggtaactatcgtcttgagtccaacccggtaagacacgacttatcgccactggcagcagccactggtaacaggattagcagagcgaggtatgtaggcggtgctacagagttcttgaagtggtggcctaactacggctacactagaaggacagtatttggtatctgcgctctgctgaagccagttaccttcggaaaaagagttggtagctcttgatccggcaaacaaaccaccgctggtagcggtggtttttttgtttgcaagcagcagattacgcgcagaaaaaaaggatctcaagaagatcctttgatcttttctacggggtctgacgctcagtggaacgaaaactcacgttaagggattttggtcatgagattatcaaaaaggatcttcacctagatccttttaaattaaaaatgaagttttaaatcaatctaaagtatatatgagtaaacttggtctgacagagaaagtctacaccttacgctgattggatttgaagttttaaatcaatctaaagtatatatgagtaaacttggtctgacagttaccaatgcttaatcagtgaggcacctatctcagcgatctgtctatttcgttcatccatagttgcctgactccccgtcgtgtagataactacgatacgggagggcttaccatctggccccagtgctgcaatgataccgcgagacccacgctcaccggctccagatttatcagcaataaaccagccagccggaagggccgagcgcagaagtggtcctgcaactttatccgcctccatccagtctattaattgttgccgggaagctagagtaagtagttcgccagttaatagtttgcgcaacgttgttgccattgctacaggcatcgtggtgtcacgctcgtcgtttggtatggcttcattcagctccggttcccaacgatcaaggcgagttacatgatcccccatgttgtgcaaaaaagcggttagctccttcggtcctccgatcgttgtcagaagtaagttggccgcagtgttatcactcatggttatggcagcactgcataattctcttactgtcatgccatccgtaagatgcttttctgtgactggtgagtactcaaccaagtcattctgagaatagtgtatgcggcgaccgagttgctcttgcccggcgtcaatacgggataataccgcgccacatagcagaactttaaaagtgctcatcattggaaaacgttcttcggggcgaaaactctcaaggatcttaccgctgttgagatccagttcgatgtaacccactcgtgcacccaactgatcttcagcatcttttactttcaccagcgtttctgggtgagcaaaaacaggaaggcaaaatgccgcaaaaaagggaataagggcgacacggaaatgttgaatactcatactcttcctttttcaatattattgaagcatttatcagggttattgtctcatgagcggatacatatttgaatgtatttagaaaaataaacaaataggggttctacaatagagttccgaggtaaacgcttttcgttcttgtctcattgccacattcataagtacccatccaagagcacgcttattcaccagggtgaaaaagcggaaacgctgtactacatcgttaaaggctctgtggcagtgctgatcaaagacgaagagggtaaagaaatgatcctctcctatctgaatcagggtgattttattggcgaactgggcctgtttgaagagggccaggaacgtagcgcatgggtacgtgcgaaaaccgcctgtgaagatatcatgcgcatgacgtcaccagacgctatgactcacccggacggcatgcaaatcaaaattacccgtcaggaaattggccagattgtcggctgctctagacaaaccgtgggacgaattcttaagatgctcgaggatcagaacacggactacgagatacctgattttacagttcagtatagcgaccagcattcacatacgattgacgcatgatattactttctgcgcacttaacttcgcatctgggcagatgatgtcgaggcgaaaaaaaatataaatcacgctaacatttgattaaaatagaacaactacaatataaaaaaactatacaaatgacaagttcttgaaaacaagaatctttttattgtcagtactgattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttacccatggttgtttatgttcggatgtgatgtgagaactgtatcctagcaagattttaaaaggaagtatatgaaagaagaacctcagtggcaaatcctaaccttttatatttctctacaggggcgcggcgtggggacaattcaacgcgtctgtgaggggagcgtttccctgctcgcaggtctgcagcgaggagccgtaatttttgcttcgcgccgtgcggccatcaaaatgtatggatgcaaatgattatacatggggatgtatgggctaaatgtacgggcgacagtcacatcatgcccctgagctgcgcacgtcaagactgtcaaggagggtattctgggcctccatgtccagagcagacagttcctttacgagattttagatccaatatcaaaggaaatgatagcattgaaggatgagactaatccaattgaggagtggcagcatatagaacagctaaagggtagtgctgaaggaagcatacgataccccgcatggaatgggataatatcacaggaggtactagactacctttcatcctacataaatagacgcatataagtacgcatttaagcataaacacgcactatgccgttcttctcatgtatatatatatacaggcaacacgcagatataggtgcgacgtgaacagtgagctgtatgtgcgcagctcgcgttgcattttcggaagcgctcgttttcggaaacgctttgaagttcctattccgaagttcctattctctagctagaaagtataggaacttcagagcgcttttgaaaaccaaaagcgctctgaagacgcactttcaaaaaaccaaaaacgcaccggactgtaacgagctactaaaatattgcgaataccgcttccacaaacattgctcaaaagtatctctttgctatatatctctgtgctatatccctatataacctacccatccacctttcgctccttgaacttgcatctaaactcgacctctacattttttatgtttatctctagtattactctttagacaaaaaaattgtagtaagaactattcatagagtgaatcgaaaacaatacgaaaatgtaaacatttcctatacgtagtatatagagacaaaatagaagaaaccgttcataattttctgaccaatgaagaatcatcaacgctatcactttctgttcacaaagtatgcgcaatccacatcggtatagaatataatcggggatgcctttatcttgaaaaaatgcacccgcagcttcgctagtaatcagtaaacgcgggaagtggagtcaggctttttttatggaagagaaaatagacaccaaagtagccttcttctaaccttaacggacctacagtgcaaaaagttatcaagagactgcattatagagcgcacaaaggagaaaaaaagtaatctaagatgctttgttagaaaaatagcgctctcgggatgcatttttgtagaacaaaaaagaagtatagattctttgttggtaaaatagcgctctcgcgttgcatttctgttctgtaaaaatgcagctcagattctttgtttgaaaaattagcgctctcgcgttgcatttttgttttacaaaaatgaagcacagattcttcgttggtaaaatagcgctttcgcgttgcatttctgttctgtaaaaatgcagctcagattctttgtttgaaaaattagcgctctcgcgttgcatttttgttctacaaaatgaagcacagatgcttcgttaacaaagatatgctattgaagtgcaagatggaaacgcagaaaatgaaccggggatgcgacgtgcaagattacctatgcaatagatgcaatagtttctccaggaaccgaaatacatacattgtcttccgtaaagcgctagactatatattattatacaggttcaaatatactatctgtttcagggaaaactcccaggttcggatgttcaaaattcaatgatgggtaacaagtacgatcgttgactactatttacgcagcagatacgatctcgtttcatcggtatcattacccccatgaacagaaatcccccttacacggaggcatcagtgaccaaacaggaaaaaaccgcccttaacatggcccgctttatcagaagccagacattaacgcttctggagaaactcaacgagctggacgcggatgaacaggcagacatctgtgaatcgcttcacgaccacgctgatgagctttaccgcagctgcc

Template pTA5 5925 bp circular limit=12:
1742_s4r anneals forward (--->) at 16
1748_s3 anneals reverse (<---) at 1397
---
Forward: 1742_s4r Reverse: 1748_s3

5acggactacgagatac...agttcctttacgagatttta3
                    ||||||||||||||||||||
                   3TCAAGGAAATGCTCTAAAAT5
5ACGGACTACGAGATAC3
 ||||||||||||||||
3tgcctgatgctctatg...tcaaggaaatgctctaaaat5

Taq DNA pol
|95°C|95°C               |    |tmf:51.4
|____|_____          72°C|72°C|tmr:51.3
|3min|30s  \ 54.6°C _____|____|45s/kb
|    |      \______/ 1:03|5min|GC 43%
|    |       30s         |    |1417bp


>1417bp_PCR_prod
ACGGACTACGAGATACctgattttacagttcagtatagcgaccagcattcacatacgattgacgcatgatattactttctgcgcacttaacttcgcatctgggcagatgatgtcgaggcgaaaaaaaatataaatcacgctaacatttgattaaaatagaacaactacaatataaaaaaactatacaaatgacaagttcttgaaaacaagaatctttttattgtcagtactgattagaaaaactcatcgagcatcaaatgaaactgcaatttattcatatcaggattatcaataccatatttttgaaaaagccgtttctgtaatgaaggagaaaactcaccgaggcagttccataggatggcaagatcctggtatcggtctgcgattccgactcgtccaacatcaatacaacctattaatttcccctcgtcaaaaataaggttatcaagtgagaaatcaccatgagtgacgactgaatccggtgagaatggcaaaagcttatgcatttctttccagacttgttcaacaggccagccattacgctcgtcatcaaaatcactcgcatcaaccaaaccgttattcattcgtgattgcgcctgagcgagacgaaatacgcgatcgctgttaaaaggacaattacaaacaggaatcgaatgcaaccggcgcaggaacactgccagcgcatcaacaatattttcacctgaatcaggatattcttctaatacctggaatgctgttttgccggggatcgcagtggtgagtaaccatgcatcatcaggagtacggataaaatgcttgatggtcggaagaggcataaattccgtcagccagtttagtctgaccatctcatctgtaacatcattggcaacgctacctttgccatgtttcagaaacaactctggcgcatcgggcttcccatacaatcgatagattgtcgcacctgattgcccgacattatcgcgagcccatttatacccatataaatcagcatccatgttggaatttaatcgcggcctcgaaacgtgagtcttttccttacccatggttgtttatgttcggatgtgatgtgagaactgtatcctagcaagattttaaaaggaagtatatgaaagaagaacctcagtggcaaatcctaaccttttatatttctctacaggggcgcggcgtggggacaattcaacgcgtctgtgaggggagcgtttccctgctcgcaggtctgcagcgaggagccgtaatttttgcttcgcgccgtgcggccatcaaaatgtatggatgcaaatgattatacatggggatgtatgggctaaatgtacgggcgacagtcacatcatgcccctgagctgcgcacgtcaagactgtcaaggagggtattctgggcctccatgtccagagcagacAGTTCCTTTACGAGATTTTA

```



# Preparations

[Pictures](https://photos.app.goo.gl/xamnimEsJigDjoPC6)

![[Yeast transformation GBM24-20240930140307093.png]]

Two yeast strains will be used for transformation:

| #     | Strain                                  | box     | pos | Start OD<sub>640</sub> |
| ----- | --------------------------------------- | ------- | --- | ---------------------- |
| µ880  | CEN.PK111-32D                           | Björn3  | 81  | 0.178                  |
| µ1877 | CEN.PK111-32D + `pTA1_TDH3_ScATF1_PGI1` | Björn12 | 26  | 0.172                  |

[[Strain information]] for  CEN.PK111-32D.

| #     | Culture OD<sub>640</sub><sup>(*)</sup> | Vol(mL) | 07:16 | 11:30                        | 13:15                        |
| ----- | -------------------------------------- | ------- | ----- | ---------------------------- | ---------------------------- |
| µ880  | 0.123                                  | 1.36    | 0.178 | = 0.154 x 5 = 0.77 (Harvest) | -                            |
| µ1877 | 0.049                                  | 3.46    | 0.172 | = 0.092 x 5 = 0.46           | = 0.152 x 5 = 0.76 (Harvest) |


<sup>(*)</sup> Culture Culture OD<sub>640</sub> is measured by mixing 1 mL of o/n culture with 45 mL of the appropriate medium and measuring the optical density against medium as blank.

# Prepare **DNA mix**

1. Take one empty and clean 1.5 mL Eppendorf tube.

| Group | ddH2O (µL) | KanMX4 PCR product (µL) |
| ----- | ---------- | ----------------------- |
| 1     | 115        | 5                       |
| 2     | 110        | 10                      |
| 3     | 105        | 15                      |
| 4     | 100        | 20                      |

2. Add the contents to the tube from the table according to your group.
3. Put the tube on ice. The DNA mix should be marked **kept on ice** until needed.


# Yeast transformation protocol

The yeast strains to be transformed are *S. cerevisiae*  [[Strain information\|CEN.PK111-32D]]  (µ880) and the same strain carrying the  `pTA1_TDH3_ScATF1_PGI1` plasmid (µ1877) made by the students in 2023.

1. Transfer 100 µL of the cell suspensions (µ880 and µ1877) to **each of two empty Eppendorf tubes** *Keep the tubes with cells on ice when you are not pipetting*.
2. Centrifuge the cells for 20-30 s at the highest speed in the microcentrifuge.
3. Remove supernatants with a P200 pipette. Leave the cell pellet at the bottom of the tube, **do not resuspend**.
4. Add 300 µL [[PEG LiAc ssDNA\|PLS]] to each of the tubes. **Put this tube back on ice**.
5. Add 60 µL of the **DNA mix** you prepared before to each tube. **Put tubes back on ice**. **Do not resuspend**.
6. Mark the tubes "880" and "1877", respectively.
7. [[vortex]] the tube until the cells are well resuspended, but **not longer**.
8. Put the tubes in a floating tube rack in a water bath at 42°C. Be sure you can identify your tube.
9. Incubate for 40 min.


During this incubation, work on your plasmid assembly.

![[in_silico.png]]


1. Remove tubes with cells from the water bath and put on ice for 1-2 min.
2. Spin tubes for 30 s to 1 min at highest speed.
4. Remove supernatant with a P1000 pipette. Leave the cell pellet at the bottom of the tube.
5. Add 400 µL YPD medium and resuspend with the pipette by **slowly** pipetting up and down using a **blue** tip, try not make foam.
6. Incubate at 30°C for 30-60 min.


![[Yeast transformation GBM24-20240930161047714.png]]

Use the time work on your plasmid assembly or on your paper presentation.

![[Yeast transformation GBM24-20241008101726788.png]]


1. Add about 1/2 mL glass spheres (~10-15 spheres) each of four empty Petri dishes with the appropriate solid medium.
2. Transfer 200 µL of the cell suspension to the Petri dish with the solid medium.
3. Add 20 µL G418 to the cell drop on the plate.
4. Spread the cells by shaking (using the [samba](https://www.youtube.com/watch?v=ArWRREJl1Rw&t=39s) method).
5. Transfer 200 µL sterile water and 20 µL of the cell suspension to another Petri dish. Add the cells to the water drop.
6. Add 20 µL G418 to the cell drop on the plate.
7. Spread the cells by shaking (using the [samba](https://www.youtube.com/watch?v=ArWRREJl1Rw&t=39s) method).
8. Mark you plates with "µ880" or "µ1877", group number, **date** and either "200 µL" or "20 µL".
9. Incubate the plates upside down for 2-3 days at 30°C.
10. Give the tubes with the rest of the cells to the instructor.

The transformation protocol is based on the [[High Efficiency Yeast Transformation Protocol\|Gietz High-efficiency yeast transformation using the LiAc/SS carrier DNA/PEG method]].

# Results

See [pictures](https://photos.app.goo.gl/xamnimEsJigDjoPC6)

If the transformation is successful, we would expect fewer colonies on the "880" plates than on
the "1877" plates.

| Course | Result | Picture                                             |
| ------ | ------ | --------------------------------------------------- |
| MGM    | µ880   | [link](https://photos.app.goo.gl/WWZueuyTTwyriiR7A) |
| MBIOAP | µ880   | [link](https://photos.app.goo.gl/LAszXNCk3SU2uRkn8) |
| MGM    | µ1877  | [link](https://photos.app.goo.gl/CU4fkMvgKaMQQu6p6) |
| MBIOAP | µ1877  | [link](https://photos.app.goo.gl/YeMN5GpYJMFzSjCJ9) |


Colonies will be picked and resuspended in 1 mL YPD medium containing 250 ppm (mg/mL) [isoamyl alcohol](https://pubchem.ncbi.nlm.nih.gov/compound/Isoamyl-alcohol) (Miller 2020).



# Reference

Miller, R. A., Lee, S., Fridmanski, E. J., Barron, E., Pence, J., Lieberman, M., & Goodson, H. V. (2020).
“Scentsor”: A Whole-Cell Yeast Biosensor with an Olfactory Reporter for Low-Cost and Equipment-Free
Detection of Pharmaceuticals. ACS Sensors, 5(10), 3025–3030. [link](https://pubs.acs.org/doi/10.1021/acssensors.0c01344)

![[download.gif]]


----




# Lista de material para a preparação de aula

- [[PEG LiAc ssDNA\|PLS]]  (0.3 mL * 2 * 4 * 2 = 4.8 mL).
- 16 * 15 = 240 µL KanMX4 PCR product made with primers 1349 and 1350.



- 40 placas de meio YPD.
- floating tube rack
- Meio YPD líquido 100 mL (6-feira dia 25)
- Água ultrapura estéril 50 mL
- Tubos FALCON 50 mL vazios estéreis.
- Micropipetas P1000, P100, P20 e P10
- Pontas amarelas, azuis e brancas novas estéreis, uma de cada cor para cada grupo.
- Tubos Eppendorf 1.5 mL **Novos**, um por grupo.
- Suporte para tubos Eppendorf, um por grupo.
- Um tubo FALCON 50 mL com ~25 mL de esferas de vidro estéreis (~ 4-5 mm grandes, para espalhar células).

- 40 Tubos vazios de vidro estéreis com tampa (tubos de cultura)
- Suportes para tubos de vidro.
- Isoamyl alcohol 0.1 - 1 mL

- Banho maria 42°C
- Microcentrífuga
- Caixas de esferovite para gelo, um por grupo.
- Marcadores
- Lamparinas, um por grupo.

YPD:
- 20 g/L peptone ou tryptone
- 10 g/L yeast extrac
- 20 g/L glucose
- 20 g/L Agar para meio sólido
