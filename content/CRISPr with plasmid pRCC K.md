### CRISPR CAS9 sgRNA plasmid

We originally asked the pCAS (https://www.addgene.org/60847) vector from the designer (jcate@lbl.gov).
Unfortunately it was "pending" and not available at the time.

This link is for the email exchange https://mail.google.com/mail/u/0/#search/crisp/KtbxLthZkGjqGBfdKMpdktVkRtbMDzfMqB

#### Search for an alternative:

I want:

- 2 micron origin of replication
- kanMX4 selection marker
- cas9 and sgRNA in the same plasmid

I made a search on [addgene](https://www.addgene.org/search/advanced/?q=Cas9&depositor=&article=&gene=&vector=&tags=&advanced_query=&results_per_page=20&page=2&selected_facets=vector_types_exact%3Ayeast-expression&sort_type=popularity):

I found these two:

- pRCC-K         10255 https://www.addgene.org/81191
- pML104-KanMx4  10959 https://www.addgene.org/83476

and an alternative system [CRISPR/Cpf1](https://www.addgene.org/browse/article/28192247).

This system has a nuclease that is different from cas9, so the scaffold sequences are different as well as some of the properties.
Among them, the nuclease produces sticky ends.

Of the two alternatives above pRCC-K seem more interesting to me. It is based
on *in-vivo* gap repair between two primer tails of a PCR product made from the
plasmid and a donor DNA 80-mer oligonucleotide. The pML104-KanMx4 is made for
ligating the sgRNA encoding DNA, which I think is less practical.


The pRCC-K is described in Generoso 2016 ([pubmed](https://www.ncbi.nlm.nih.gov/pubmed/27327211), [pdf](https://www.sciencedirect.com/science/article/pii/S016770121630149X?via%3Dihub)) supplementary [material](https://ars.els-cdn.com/content/image/1-s2.0-S016770121630149X-mmc1.pdf)

The paper describe **four** different plasmids. Two plasmids with two differen
marker genes, natMX4 and kanMX4 for one or two sgRNA sequences. The plasmids
for two sgRNA sequences seem to be tricky to use as it needs digestion with
NotI or EcoRI prior to PCR.

This leaves the pRCC-K as the best alternative ([[pRCC_K.gb|sequence]]).

#### Described use

The paper describes the deletion of ILV1, LEU4 and LEU9 genes.
The primers used are available in Table S1:

```

>CC-Ilv1_Fw Incorporation of ILV1 protospacer in pRCC_K
GTTACTTTACCCGACGTCCCGTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG
>CC-Ilv1_Rv Incorporation of ILV1 protospacer in pRCC_K
GGGACGTCGGGTAAAGTAACGATCATTTATCTTTCACTGCGGAG
>DR-Ilv1 Donor for ILV1 deletion
CAAGCCACATTTAAACTAAGTCAATTACACAAAGTTAGTGAACCGACAATTTACTTTATAAATTTACGCAACAACTTGTT

>A1-Ilv1 Control PCR for ILV1 deletion (promoter)
AATTCACTAGCGGCTCCTTG
>A4-Ilv1 Control PCR for ILV1 deletion (terminator)
ATGGCTATGTGGAAGAAGTC

>CC-Leu4/9_Fw Incorporation of LEU4/9 protospacer in pRCC_K
TGTCACAATGACCGTGGTTGGTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG
>CC-Leu4/9_Rv Incorporation of LEU4/9 protospacer in pRCC_K
CAACCACGGTCATTGTGACAGATCATTTATCTTTCACTGCGGAG
>DR-Leu4 Donor for LEU4 deletion
TACTGTAGACTTTTTCCTTACAAAAAGACAAGGAACAATCGAACTTTTCTGTATTTCAGGACTTATTCGCTTCTATTTAT

>DR-Leu9 Donor for LEU9 deletion
GGATAATACTATCGGCACATTATCATTTAGCCGCGTAGCCTAGAAAGGAGTAGCTTATGATTACTCATGTTATATATATA

>A1-Leu4 Control PCR for LEU4deletion (promoter)
TTGTACAGTAACGGCCAGTC
>A4-Leu4 Control PCR for LEU4deletion (terminator)
TTCGTCACTAACCGCCAAAC
>A1-Leu9 Control PCR for LEU9deletion (promoter)
GGTAACGGTCGTAGTGAATG
>A4-Leu9 Control PCR for LEU9deletion (terminator)
TGTTCTCCCTTCACAAAGTC

```

For targeting the ILV1, primers CC-Ilv1_Fw  and CC-Ilv1_Rv were used to amplify the pRCC-K:

They bind to the circular template in this way:

```

    5GTTACTTTACCCGACGTCCCGTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG3
                         ||||||||||||||||||||||||||||||||||| tm 55.8 (dbd) 67.5
                        5CGTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG...CTCCGCAGTGAAAGATAAATGATCG3
                        3GCAAAATCTCGATCTTTATCGTTCAATTTTATTCC...GAGGCGTCACTTTCTATTTACTAGC5
                                                               ||||||||||||||||||||||||| tm 54.5 (dbd) 69.5
                                                              3GAGGCGTCACTTTCTATTTACTAGCAATGAAATGGGCTGCAGGG5

```

The primers form a PCR product that recombine with itself in-vivo to form a circular sequence:

```
                              GTTACTTTACCCGACGTCCCGTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG_____
                              CAATGAAATGGGCTGCAGGGCAAAATCTCGATCTTTATCGTTCAATTTTATTCC____ |
                                                                                        ||
 _____CTCCGCAGTGAAAGATAAATGATCGTTACTTTACCCGACGTCCC                                      ||
| ____GAGGCGTCACTTTCTATTTACTAGCAATGAAATGGGCTGCAGGG                                      ||
||                                                                                      ||
||         SNR52 promoter --->                    ======== sgRNA scaffold ==========    ||
||______________________________________________________________________________________||
|________________________________________________________________________________________|


                              GTTACTTTACCCGACGT-CCC
                              CAATGAAATGGGCTGCA-GGG
                                               |
                                              cu
                                              site
```

The sequence `GTTTTAGAGCTAGAAATAGCAAGTTAAAATAAGG` is the sgRNA scaffold
sequence necessary for the recognition by cas9. This part is always the same.
The tails of the primers is the spacer sequence needed for the recognition of
the gene by the sgRNA molecule. We can find this in the ILV1 sequence below (in
CAPS):
```

>ILV1 YER086W SGDID:S000000888
atgtcagctactctactaaagcaaccattatgtacggttgttcggcaaggtaaacagtccaaagtgtctggattgaacc
ttttgagactaaaggctcatttgcacagacaacacctgtcaccttccttgataaaactacactctgaattgaaattgga
tgagctgcaaactgataacacccctgattacgtccgtttagttttaaggtcctctgtatacgatgttattaatgaatc
ccaatctctcaaggtgtaggtttgtcttcccgtctaaacacgaatgtcatcttgaaaagagaagatctattgcctg
tctctttcaagcttcgtggtgcctataacatgattgccaagttggacgattctcaaagaaaccagggtgttattgcctg
ttcagctgggaatcatgcccaaggtgtggcctttgctgctaaacacttgaaaatacctgctactatcgttatgcctg
tgtacaccatctattaagtatcaaaatgtctcgagattagggtctcaagtcgtcctatatggtaacgattttgacgagg
ctaaggctgaatgtgccaaattggctgaagagcgtggcttgacgaacattcctcctttcgatcatccttatgtcattgc
cggtcaaggtactgtagctatggaaatcctaagacaagtacgtaccgctaataagatcggtgctgtctttgttcccgtc
ggcggtggtggtttaattgctggtattggtgcttatttgaaaagggttgctcctcatatcaaaatcattggtgttgaaa
cttacgatgcggccactttacataattccttgcaacgcaaccagagaactcctttacctgtggtgggtacttttgccga
tggtacgtctgtgcgtatgattggtgaagaaacatttagagtcgcccaacaagtggttgatgaagttgttcttgttaac
actgacgaaatctgtgctgcagtaaaggatatttttgaagatactagaagtattgtagaaccatctggtgccctttcag
tagccggtatgaagaaatacatctctaccgtacatccagaaattgaccacactaaaaacacctatgttcccatcctttc
tggtgctaacatgaactttgatagattaagatttgtttccgaacgtgctgttcttggtgaaggaaaggaagtcttcatg
ttaGTTACTTTACCCGACGTCCCtggtgcgttcaagaaaatgcaaaagatcatccacccaagatctgtcactgaattc
   ----------------||--PAM
cttaccgttacaatgaacatcgtcatgagtcctctagtgaagtgcccaaggcttacatttacacttctttcagcgtcg
tgacagagaaaaggaaatcaagcaagttatgcaacagttgaatgctttaggttttgaagctgtggatatctccgataac
gaattggctaaatctcatggtagatacttggttggtggtgcttctaaggttcctaatgaaagaattatttcatttgaa
tccctgaaagaccaggtgccttgactaggttccttggaggcctaagcgattcttggaatcttactttattccattatag
aaaccatggtgccgatatcggtaaggttttagctggtatttccgttcctccaagggaaaacttaaccttccaaaaattc
ttggaagatttaggctacacttatcatgatgaaactgataacactgtttatcaaaaattcttgaaatattaa


```

#### PAM

The cas9 needs there to be a PAM sequence (NGG for cas9) immediately after the
spacer sequence. in the sequence above, we can spot "tgg" after the spacer
sequence.


#### Donor DNA

The donor DNA for the ILV1 gene is the following 80-mer oligonucleotide.

```
LOCUS       New_DNA                   80 bp ds-DNA     linear       07-OCT-2019
DEFINITION  .
ACCESSION
VERSION
SOURCE      .
  ORGANISM  .
COMMENT
COMMENT     ApEinfo:methylated:1
FEATURES             Location/Qualifiers
     misc_feature    42..80
                     /locus_tag="New Feature"
                     /label="New Feature"
                     /ApEinfo_label="New Feature"
                     /ApEinfo_fwdcolor="cyan"
                     /ApEinfo_revcolor="green"
                     /ApEinfo_graphicformat="arrow_data {{0 1 2 0 0 -1} {} 0}
                     width 5 offset 0"
     misc_feature    1..41
                     /locus_tag="New Feature(1)"
                     /label="New Feature(1)"
                     /ApEinfo_label="New Feature"
                     /ApEinfo_fwdcolor="#00ff46"
                     /ApEinfo_revcolor="green"
                     /ApEinfo_graphicformat="arrow_data {{0 1 2 0 0 -1} {} 0}
                     width 5 offset 0"
ORIGIN
        1 CAAGCCACAT TTAAACTAAG TCAATTACAC AAAGTTAGTG AACCGACAAT TTACTTTATA
       61 AATTTACGCA ACAACTTGTT
//
```


The features marked corresponds to 40 nucelotides before and 40 nucleotides
after the ILV1 open reading frame, marked by features in the sequence below.

```
LOCUS       ILV1_YER086W_SGD        1815 bp ds-DNA     linear       07-OCT-2019
DEFINITION  .
ACCESSION
VERSION
SOURCE      .
  ORGANISM  .
COMMENT     >ILV1 YER086W SGDID:S000000888, chrV:328477..330207+/- 1kb
COMMENT     ApEinfo:methylated:1
FEATURES             Location/Qualifiers
     misc_feature    1774..1812
                     /locus_tag="New Feature"
                     /label="New Feature"
                     /ApEinfo_label="New Feature"
                     /ApEinfo_fwdcolor="cyan"
                     /ApEinfo_revcolor="green"
                     /ApEinfo_graphicformat="arrow_data {{0 1 2 0 0 -1} {} 0}
                     width 5 offset 0"
     misc_feature    3..43
                     /locus_tag="New Feature(1)"
                     /label="New Feature(1)"
                     /ApEinfo_label="New Feature"
                     /ApEinfo_fwdcolor="cyan"
                     /ApEinfo_revcolor="green"
                     /ApEinfo_graphicformat="arrow_data {{0 1 2 0 0 -1} {} 0}
                     width 5 offset 0"
     misc_feature    43..1772
                     /locus_tag="ILV1_orf"
                     /label="ILV1_orf"
                     /ApEinfo_label="ILV1_orf"
                     /ApEinfo_fwdcolor="#c9ff4b"
                     /ApEinfo_revcolor="green"
                     /ApEinfo_graphicformat="arrow_data {{0 1 2 0 0 -1} {} 0}
                     width 5 offset 0"
ORIGIN
        1 TACAAGCCAC ATTTAAACTA AGTCAATTAC ACAAAGTTAG TGATGTCAGC TACTCTACTA
       61 AAGCAACCAT TATGTACGGT TGTTCGGCAA GGTAAACAGT CCAAAGTGTC TGGATTGAAC
      121 CTTTTGAGAC TAAAGGCTCA TTTGCACAGA CAACACCTGT CACCTTCCTT GATAAAACTA
      181 CACTCTGAAT TGAAATTGGA TGAGCTGCAA ACTGATAACA CCCCTGATTA CGTCCGTTTA
      241 GTTTTAAGGT CCTCTGTATA CGATGTTATT AATGAATCTC CAATCTCTCA AGGTGTAGGT
      301 TTGTCTTCCC GTCTAAACAC GAATGTCATC TTGAAAAGAG AAGATCTATT GCCTGTTTTC
      361 TCTTTCAAGC TTCGTGGTGC CTATAACATG ATTGCCAAGT TGGACGATTC TCAAAGAAAC
      421 CAGGGTGTTA TTGCCTGTTC AGCTGGGAAT CATGCCCAAG GTGTGGCCTT TGCTGCTAAA
      481 CACTTGAAAA TACCTGCTAC TATCGTTATG CCTGTTTGTA CACCATCTAT TAAGTATCAA
      541 AATGTCTCGA GATTAGGGTC TCAAGTCGTC CTATATGGTA ACGATTTTGA CGAGGCTAAG
      601 GCTGAATGTG CCAAATTGGC TGAAGAGCGT GGCTTGACGA ACATTCCTCC TTTCGATCAT
      661 CCTTATGTCA TTGCCGGTCA AGGTACTGTA GCTATGGAAA TCCTAAGACA AGTACGTACC
      721 GCTAATAAGA TCGGTGCTGT CTTTGTTCCC GTCGGCGGTG GTGGTTTAAT TGCTGGTATT
      781 GGTGCTTATT TGAAAAGGGT TGCTCCTCAT ATCAAAATCA TTGGTGTTGA AACTTACGAT
      841 GCGGCCACTT TACATAATTC CTTGCAACGC AACCAGAGAA CTCCTTTACC TGTGGTGGGT
      901 ACTTTTGCCG ATGGTACGTC TGTGCGTATG ATTGGTGAAG AAACATTTAG AGTCGCCCAA
      961 CAAGTGGTTG ATGAAGTTGT TCTTGTTAAC ACTGACGAAA TCTGTGCTGC AGTAAAGGAT
     1021 ATTTTTGAAG ATACTAGAAG TATTGTAGAA CCATCTGGTG CCCTTTCAGT AGCCGGTATG
     1081 AAGAAATACA TCTCTACCGT ACATCCAGAA ATTGACCACA CTAAAAACAC CTATGTTCCC
     1141 ATCCTTTCTG GTGCTAACAT GAACTTTGAT AGATTAAGAT TTGTTTCCGA ACGTGCTGTT
     1201 CTTGGTGAAG GAAAGGAAGT CTTCATGTTA GTTACTTTAC CCGACGTCCC TGGTGCGTTC
     1261 AAGAAAATGC AAAAGATCAT CCACCCAAGA TCTGTCACTG AATTCTCTTA CCGTTACAAT
     1321 GAACATCGTC ATGAGTCCTC TAGTGAAGTG CCCAAGGCTT ACATTTACAC TTCTTTCAGC
     1381 GTCGTTGACA GAGAAAAGGA AATCAAGCAA GTTATGCAAC AGTTGAATGC TTTAGGTTTT
     1441 GAAGCTGTGG ATATCTCCGA TAACGAATTG GCTAAATCTC ATGGTAGATA CTTGGTTGGT
     1501 GGTGCTTCTA AGGTTCCTAA TGAAAGAATT ATTTCATTTG AATTCCCTGA AAGACCAGGT
     1561 GCCTTGACTA GGTTCCTTGG AGGCCTAAGC GATTCTTGGA ATCTTACTTT ATTCCATTAT
     1621 AGAAACCATG GTGCCGATAT CGGTAAGGTT TTAGCTGGTA TTTCCGTTCC TCCAAGGGAA
     1681 AACTTAACCT TCCAAAAATT CTTGGAAGAT TTAGGCTACA CTTATCATGA TGAAACTGAT
     1741 AACACTGTTT ATCAAAAATT CTTGAAATAT TAAACCGACA ATTTACTTTA TAAATTTACG
     1801 CAACAACTTG TTAGG
//

```

#### Deletion of ScFAA1

The constant parts of the primers were extracted below, the tail1 and tail2
needs to be replaced by a spacer sequence specific for ScFAA1.

    >CC-FAA1_Fw
    tail1-gttttagagctagaaatagcaagttaaaataagg

    >CC-FAA1_Rv
    tail2-gatcatttatctttcactgcggag

The paper suggests a web based tool for selecting spacer sequences (https://www.dna20.com/eCommerce/cas9/input).
There is now a redirection to this url (https://www.atum.bio/eCommerce/cas9/input) which i used.
The best result was ATCCCTGGTGGCGGCGCCTT , according to the scoring (100).

- [[tool1.png|Initial page]]

- [[tool2.png|Results page]]

The spacer was incorporated
with the rest of the primer like this:

    >CC-FAA1_Fw 54-mer
    ATCCCTGGTGGCGGCGCCTTgttttagagctagaaatagcaagttaaaataagg

    >CC-FAA1_Rv 44-mer
    AAGGCGCCGCCACCAGGGATgatcatttatctttcactgcggag

