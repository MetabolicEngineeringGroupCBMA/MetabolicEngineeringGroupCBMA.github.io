# LAB10 Plasmid miniprep & restriction digestion

[[material#LAB10]]

Summary:
- cut DNA with restriction enzymes, one enzyme per group.
- Plasmid miniprep using a commercial kit for DNA sequencing.
- Run agarose gel#5 on plasmid DNA and digested plasmid DNA

| Table#6 | Group | Enzyme mix    |
| ------- | ----- | ------------- |
|         | 1     | AjiI          |
|         | 4     | EcoRI         |
|         | 3     | EcoRV(Eco32I) |

Enzyme mix = 5 µL Enzyme + 5 µL buffer x10

#### Restriction digestion (One per group)

- Pipette 8 µL of the plasmid solution into a new Eppendorf tube.
- Mark the Eppendorf tube
- Ask your teacher to add 2 µL of Restriction enzyme mix (Table#6) to your tube.
- Spin and incubate for one hour at 37°C. **During this incubation, do the plasmid preparation below.**

#### Miniprep, one per group

Preparation of  plasmids  using a commercial alkaline lysis mini prep kit. The teacher has prepared *E. coli* cultures in liquid medium beforehand. Cultures with each plasmid were grown in or on [[LB]] with [[antibiotics]] for selection of the plasmids. We will use the  [[MB010_NZYMiniprep.pdf|NZYMiniprep]].


![[pTAx/EGB25_002.png|580x1087]]

#### Agarose gel electrophoresis of plasmid DNA and plasmid digestion

- Put a 2 µL drop of [[6x DNA loading buffer]] on a piece of Parafilm.
- Add 6 µL of plasmid DNA to the drop
- Put the gel in the gel tray.
- Add more buffer (if needed) until the gel is just submerged.
- Add all of the DNA to an empty well, start with the leftmost well.
- Take note of where your samples are.
- The teacher will load the molecular weight marker.
- Apply the electrical field as soon as you are done.
- The electrophoresis last around 15 - 20 min.
- When the gel run is completed, the teacher with take a picture using a [[GenoSmart\|transilluminator]].




![[pTAx/EGB25_001-3.png]]


| 📌  | Sample                | 📝     | µL  |  😶 |     |
| --- | --------------------- | ------ | --- | --: | --: |
|     | GeneRuler 1 kb ladder |        | 3   |     |     |
|     | pTA7 candidate        | α      | 6   |  👽 |     |
|     | ✂️ AjiI               | AjiI   | "   |     |     |
|     | ✂️ EcoRI              | EcoRI  | "   |     |     |
|     | ✂️ Eco32I             | Eco32I | "   |     |     |
|     | pTA7 candidate        | β      | "   |  🥳 |     |
|     | ✂️ AjiI               | AjiI   | "   |     |     |
|     | ✂️ EcoRI              | EcoRI  | "   |     |     |
|     | ✂️ Eco32I             | Eco32I | "   |     |     |
|     | pTA7 candidate        | ∆      | "   |  🥳 |     |
|     | ✂️ AjiI               | AjiI   | "   |     |     |
|     | ✂️ EcoRI              | EcoRI  | "   |     |     |
|     | ✂️ Eco32I             | Eco32I | "   |     |     |
|     | pTA7 candidate        | ε      | "   |  🥳 |     |
|     | ✂️ AjiI               | AjiI   | "   |     |     |
|     | ✂️ EcoRI              | EcoRI  | "   |     |     |
|     | ✂️ Eco32I             | Eco32I | "   |     |     |
|     | GeneRuler 1 kb ladder |        | 3   |     |     |
|     | NZYMiniprep           | α      |     |     |     |
|     | ""                    | β      |     |     |     |
|     | ""                    | ∆      |     |     |     |
|     | ""                    | ε      |     |     |     |

Gel: [[NZYMiniprep]],  elution 50 µL warm AE buffer.

![](GeneRuler_1_kb_DNA_Ladder.png)



```

LOCUS       pTA7                    5450 bp    DNA     circular UNK 01-JAN-1980
DEFINITION  amp pbr crp∆ 2µ TRP1.
ACCESSION   id_rc
VERSION     id_rc
KEYWORDS    .
SOURCE
  ORGANISM  .
            .
COMMENT     pydna cdseguid=xbRMZpY-PTfFNKgRULL-_Na0Pu0 2024-06-07T15:21:53
            ZraI:1
            AatII:1
            EcoRV:2
            FspAI:1
FEATURES             Location/Qualifiers
     primer_bind     complement(66..94)
                     /label="865_pYPKpwR"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     primer_bind     114..143
                     /label="866_pYPKpwF"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     promoter        complement(262..281)
                     /note="pLannotate"
                     /database="snapgene"
                     /identity="100.0"
                     /match_length="44.4"
                     /fragment="True"
                     /other="promoter"
                     /locus_tag="T5 promoter (fragment)"
                     /label="T5 promoter (fragment)"
                     /ApEinfo_label="T5 promoter (fragment)"
                     /ApEinfo_fwdcolor="#EE92FE"
                     /ApEinfo_revcolor="#EE92FE"
                     /ApEinfo_graphicformat="arrow_data {{0 0.5 0 1 2 0 0 -1 0
                     -0.5} {} 0} width 5 offset 0"
     primer_bind     complement(339..355)
                     /label="977_Crp.REV"
                     /PCR_conditions="primer
                     sequence:TACAATAGAGTTCCGAGGTAAACGCTTTTCGTTCTTGTCTCATTGCC"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     misc_binding    386..389
                     /bound_moiety="echinomycin"
     misc_binding    401..404
                     /bound_moiety="echinomycin"
     misc_binding    412..415
                     /bound_moiety="echinomycin"
     misc_binding    417..420
                     /bound_moiety="echinomycin"
     misc_binding    429..432
                     /bound_moiety="echinomycin"
     primer_bind     446..470
                     /label="1113_Amp.fw.nw"
                     /PCR_conditions="primer
                     sequence:GAAAAGCGTTTACCTCGGAACTCTATTGTAGAACCCCTATTTGTTTATTT
                     TTCTA"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     regulatory      506..512
                     /regulatory_class="promoter"
                     /note="promoter P3 (6)"
     regulatory      535..539
                     /regulatory_class="ribosome_binding_site"
                     /note="Shine-Dalgarno sequence"
     gene            547..1407
                     /gene="bla"
     CDS             547..1407
                     /gene="bla"
                     /note="E-286"
                     /codon_start=1
                     /transl_table=11
                     /product="beta-lactamase"
                     /protein_id="AAB59737.1"
                     /translation="MSIQHFRVALIPFFAAFCLPVFAHPETLVKVKDAEDQLGARVGYI
                     ELDLNSGKILESFRPEERFPMMSTFKVLLCGAVLSRVDAGQEQLGRRIHYSQNDLVEYS
                     PVTEKHLTDGMTVRELCSAAITMSDNTAANLLLTTIGGPKELTAFLHNMGDHVTRLDRW
                     EPELNEAIPNDERDTTMPAAMATTLRKLLTGELLTLASRQQLIDWMEADKVAGPLLRSA
                     LPAGWFIADKSGAGERGSRGIIAALGPDGKPSRIVVIYTTGSQATMDERNRQIAEIGAS
                     LIKHW"
     sig_peptide     547..615
                     /gene="bla"
     mat_peptide     616..1404
                     /gene="bla"
                     /product="beta-lactamase"
     primer_bind     complement(1436..1457)
                     /label="987_Amp.REV"
                     /PCR_conditions="primer
                     sequence:AGAAAGTCTACACCTTACGCTGATTGGATTTGAAGTTTTAAATCAATCTA
                     AA"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     primer_bind     1487..1505
                     /label="1196_Pbr.FW"
                     /PCR_conditions="primer
                     sequence:AATCCAATCAGCGTAAGGTGTAGACTTTCTCTGTCAGACCAAGTTTACT"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     repeat_region   complement(1594..1631)
                     /note="corresponds to one of the 38bp repeats found in Tn3
                     (bp 1-38 and complement (4920-4957))"
                     /rpt_type=inverted
     old_sequence    complement(2049..2050)
                     /note="revision according to (17)"
                     /citation=[2]
                     /citation=[17]
                     /replace="at"
     old_sequence    complement(2049)
                     /note="revision according to (16)"
                     /citation=[2]
                     /citation=[16]
                     /citation=[17]
                     /replace="t"
     old_sequence    complement(2050)
                     /citation=[17]
     rep_origin      complement(2244)
     misc_binding    complement(2332..2340)
                     /bound_moiety="dnaA"
     misc_feature    2365..2428
                     /note="L-strand Y effector site"
                     /citation=[5]
     repeat_region   2530..2534
                     /note="gamma-delta insertion target sequence"
                     /rpt_type=direc
     misc_feature    complement(2612..2768)
                     /note="H-strand Y effector site"
                     /citation=[5]
     CDS             complement(2673..2864)
                     /codon_start=1
                     /transl_table=11
                     /product="ROP protein"
                     /protein_id="AAB59736.1"
                     /translation="MTKQEKTALNMARFIRSQTLTLLEKLNELDADEQADICESLHDHA
                     DELYRSCLARFGDDGENL"
     old_sequence    complement(2864..2865)
                     /citation=[17]
     misc_difference complement(2865..2866)
                     /note="conflict"
                     /citation=[23]
                     /replace="caa"
     regulatory      complement(2869..2874)
                     /regulatory_class="ribosome_binding_site"
     regulatory      complement(2870..2874)
                     /regulatory_class="ribosome_binding_site"
                     /note="Shine-Dalgarno sequence"
     old_sequence    complement(2886..2887)
                     /citation=[2]
                     /citation=[22]
     misc_difference complement(2887..2888)
                     /note="conflict"
                     /citation=[23]
                     /replace="att"
     primer_bind     2895..2913
                     /label="984_Micron.FW"
                     /PCR_conditions="primer
                     sequence:ATCGTATCTGCTGCGTAAATAGTAGTCAACGATCGTACTTGTTACCCAT"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     primer_bind     complement(2910..2924)
                     /label="1195_Pbr.REV"
                     /PCR_conditions="primer
                     sequence:GTTGACTACTATTTACGCAGCAGATACGATCTCGTTTCATCGGT"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     rep_origin      3134..4480
                     /note="yeast 2μ plasmid origin of replication"
                     /note="color: #ffff00"
                     /label="2μ ori"
     primer_bind     complement(4461..4478)
                     /label="983_Micron.REV"
                     /PCR_conditions="primer
                     sequence:CAGAGCAGACAGTTCCTTTACGAGATTTTAGATCCAATATCAAAGGAA"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     primer_bind     4569..4589
                     /label="1804_TRP1fp_pTA"
                     /PCR_conditions="primer
                     sequence:TAAAATCTCGTAAAGGAACTGTCTGCTCTGtataaaaataggcgtatcac
                     g"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     promoter        4595..4696
                     /gene="S. cerevisiae TRP1"
                     /label="TRP1 promoter"
                     /note="color: #ffffff"
     CDS             4697..5371
                     /codon_start=1
                     /gene="S. cerevisiae TRP1"
                     /note="yeast auxotrophic marker"
                     /note="color: #ff7f50"
                     /product="phosphoribosylanthranilate isomerase, required
                     for tryptophan biosynthesis"
                     /transl_table=1
                     /translation="MSVINFTGSSGPLVKVCGLQSTEAAECALDSDADLLGIICVPNRK
                     RTIDPVIARKISSLVKAYKNSSGTPKYLVGVFRNQPKEDVLALVNDYGIDIVQLHGDES
                     WQEYQEFLGLPVIKRLVFPKDCNILLSAASQKPHSFIPLFDSEAGGTGELLDWNSISDW
                     VGRQESPESLHFMLAGGLTPENVGDALRLNGVIGVDVSGGVETNGVKDSNKIANFVKNA
                     KK*"
                     /label="TRP1"
     rep_origin      complement(5210..5450)
                     /note="S. cerevisiae autonomously replicating sequence
                     ARS1/ARS416"
                     /note="color: #ffff00"
                     /label="ARS1"
     primer_bind     5421..5436
                     /label="978_Crp.FW"
                     /PCR_conditions="primer
                     sequence:AACTGTAAAATCAGGTATCTCGTAGTCCGTGTTCTGATCCTCGAGC"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
     primer_bind     complement(5430..5450)
                     /label="1347_TRP1rp_pTA"
                     /PCR_conditions="primer
                     sequence:ACGGACTACGAGATACCTGATTTTACAGTTGATCTTTTATGCTTGCTTTT
                     C"
                     /ApEinfo_fwdcolor="#baffa3"
                     /ApEinfo_revcolor="#ffbaba"
ORIGIN
        1 gttctgatcc tcgagcatct taagaattcg tcccacggtt tgtctagagc agccgacaa
       61 ctggccaatt tcctgacggg taattttgat ttgcatgccg tccgggtgag tcatagcgtc
      121 tggtgacgtc atgcgcatga tatcttcaca ggcggttttc gcacgtaccc atgcgctacg
      181 ttcctggccc tcttcaaaca ggcccagttc gccaataaaa tcaccctgat tcagatagga
      241 gaggatcatt tctttaccct cttcgtcttt gatcagcact gccacagagc ctttaacga
      301 gtagtacagc gtttccgctt tttcaccctg gtgaataagc gtgctcttgg atgggtac
      361 atgaatgtgg caatgagaca agaacgaaaa gcgtttacct cggaactcta ttgtagaacc
      421 cctatttgtt tatttttcta aatacattca aatatgtatc cgctcatgag acaataaccc
      481 tgataaatgc ttcaataata ttgaaaaagg aagagtatga gtattcaaca tttccgtgtc
      541 gcccttattc ccttttttgc ggcattttgc cttcctgttt ttgctcaccc agaaacgctg
      601 gtgaaagtaa aagatgctga agatcagttg ggtgcacgag tgggttacat cgaactgga
      661 ctcaacagcg gtaagatcct tgagagtttt cgccccgaag aacgttttcc aatgatgagc
      721 acttttaaag ttctgctatg tggcgcggta ttatcccgtg ttgacgccgg gcaagagcaa
      781 ctcggtcgcc gcatacacta ttctcagaat gacttggttg agtactcacc agtcacagaa
      841 aagcatctta cggatggcat gacagtaaga gaattatgca gtgctgccat aaccatgag
      901 gataacactg cggccaactt acttctgaca acgatcggag gaccgaagga gctaaccgc
      961 tttttgcaca acatggggga tcatgtaact cgccttgatc gttgggaacc ggagctgaa
     1021 gaagccatac caaacgacga gcgtgacacc acgatgcctg cagcaatggc aacaacgttg
     1081 cgcaaactat taactggcga actacttact ctagcttccc ggcaacaatt aatagactgg
     1141 atggaggcgg ataaagttgc aggaccactt ctgcgctcgg cccttccggc tggctgg
     1201 attgctgata aatctggagc cggtgagcgt gggtctcgcg gtatcattgc agcactgggg
     1261 ccagatggta agccctcccg tatcgtagtt atctacacga cggggagtca ggcaactatg
     1321 gatgaacgaa atagacagat cgctgagata ggtgcctcac tgattaagca ttggtaactg
     1381 tcagaccaag tttactcata tatactttag attgatttaa aacttcaaat ccaatcagcg
     1441 taaggtgtag actttctctg tcagaccaag tttactcata tatactttag attgatttaa
     1501 aacttcattt ttaatttaaa aggatctagg tgaagatcct ttttgataat ctcatgacca
     1561 aaatccctta acgtgagttt tcgttccact gagcgtcaga ccccgtagaa aagatcaaag
     1621 gatcttcttg agatcctttt tttctgcgcg taatctgctg cttgcaaaca aaaaaaccac
     1681 cgctaccagc ggtggtttgt ttgccggatc aagagctacc aactcttttt ccgaaggtaa
     1741 ctggcttcag cagagcgcag ataccaaata ctgtccttct agtgtagccg tagttaggcc
     1801 accacttcaa gaactctgta gcaccgccta catacctcgc tctgctaatc ctgttaccag
     1861 tggctgctgc cagtggcgat aagtcgtgtc ttaccgggtt ggactcaaga cgatagttac
     1921 cggataaggc gcagcggtcg ggctgaacgg ggggttcgtg cacacagccc agcttggagc
     1981 gaacgaccta caccgaactg agatacctac agcgtgagct atgagaaagc gccacgcttc
     2041 ccgaagggag aaaggcggac aggtatccgg taagcggcag ggtcggaaca ggagagcgca
     2101 cgagggagct tccaggggga aacgcctggt atctttatag tcctgtcggg tttcgccacc
     2161 tctgacttga gcgtcgattt ttgtgatgct cgtcaggggg gcggagccta tggaaaaacg
     2221 ccagcaacgc ggccttttta cggttcctgg ccttttgctg gccttttgct cacatgttc
     2281 ttcctgcgtt atcccctgat tctgtggata accgtattac cgcctttgag tgagctgata
     2341 ccgctcgccg cagccgaacg accgagcgca gcgagtcagt gagcgaggaa gcggaagagc
     2401 gcctgatgcg gtattttctc cttacgcatc tgtgcggtat ttcacaccgc atatggtgca
     2461 ctctcagtac aatctgctct gatgccgcat agttaagcca gtatacactc cgctatcgc
     2521 acgtgactgg gtcatggctg cgccccgaca cccgccaaca cccgctgacg cgccctgacg
     2581 ggcttgtctg ctcccggcat ccgcttacag acaagctgtg accgtctccg ggagctgca
     2641 gtgtcagagg ttttcaccgt catcaccgaa acgcgcgagg cagctgcggt aaagctcatc
     2701 agcgtggtcg tgaagcgatt cacagatgtc tgcctgttca tccgcgtcca gctcgttgag
     2761 tttctccaga agcgttaatg tctggcttct gataaagcgg gccatgttaa gggcgg
     2821 ttcctgtttg gtcactgatg cctccgtgta agggggattt ctgttcatgg gggtaatga
     2881 accgatgaaa cgagatcgta tctgctgcgt aaatagtagt caacgatcgt acttgttacc
     2941 catcattgaa ttttgaacat ccgaacctgg gagttttccc tgaaacagat agtatatttg
     3001 aacctgtata ataatatata gtctagcgct ttacggaaga caatgtatgt atttcggttc
     3061 ctggagaaac tattgcatct attgcatagg taatcttgca cgtcgcatcc ccggttca
     3121 ttctgcgttt ccatcttgca cttcaatagc atatctttgt taacgaagca tctgtgcttc
     3181 attttgtaga acaaaaatgc aacgcgagag cgctaatttt tcaaacaaag aatctgagc
     3241 gcatttttac agaacagaaa tgcaacgcga aagcgctatt ttaccaacga agaatctgtg
     3301 cttcattttt gtaaaacaaa aatgcaacgc gagagcgcta atttttcaaa caaagaatc
     3361 gagctgcatt tttacagaac agaaatgcaa cgcgagagcg ctattttacc aacaaagaa
     3421 ctatacttct tttttgttct acaaaaatgc atcccgagag cgctattttt ctaacaaagc
     3481 atcttagatt actttttttc tcctttgtgc gctctataat gcagtctctt gataac
     3541 tgcactgtag gtccgttaag gttagaagaa ggctactttg gtgtctattt tctcttcca
     3601 aaaaaaagcc tgactccact tcccgcgttt actgattact agcgaagctg cgggtgca
     3661 ttttcaagat aaaggcatcc ccgattatat tctataccga tgtggattgc gcatactttg
     3721 tgaacagaaa gtgatagcgt tgatgattct tcattggtca gaaaattatg aacggtttc
     3781 tctattttgt ctctatatac tacgtatagg aaatgtttac attttcgtat tgttttcga
     3841 tcactctatg aatagttctt actacaattt ttttgtctaa agagtaatac tagagataaa
     3901 cataaaaaat gtagaggtcg agtttagatg caagttcaag gagcgaaagg tggatgggta
     3961 ggttatatag ggatatagca cagagatata tagcaaagag atacttttga gcaatgtttg
     4021 tggaagcggt attcgcaata ttttagtagc tcgttacagt ccggtgcgtt tttgg
     4081 tgaaagtgcg tcttcagagc gcttttggtt ttcaaaagcg ctctgaagtt cctatac
     4141 ctagctagag aataggaact tcggaatagg aacttcaaag cgtttccgaa aacgagcgc
     4201 tccgaaaatg caacgcgagc tgcgcacata cagctcactg ttcacgtcgc acctatatc
     4261 gcgtgttgcc tgtatatata tatacatgag aagaacggca tagtgcgtgt ttatgcttaa
     4321 atgcgtactt atatgcgtct atttatgtag gatgaaaggt agtctagtac ctcctgtga
     4381 attatcccat tccatgcggg gtatcgtatg cttccttcag cactaccctt tagctgttc
     4441 atatgctgcc actcctcaat tggattagtc tcatccttca atgctatcat ttcctttga
     4501 attggatcta aaatctcgta aaggaactgt ctgctctgta taaaaatagg cgtatcacga
     4561 ggccaattcg gtcgaaaaaa gaaaaggaga gggccaagag ggagggcatt ggtgacta
     4621 gagcacgtga gtatacgtga ttaagcacac aaaggcagct tggagtatgt ctgttattaa
     4681 tttcacaggt agttctggtc cattggtgaa agtttgcggc ttgcagagca cagaggccgc
     4741 agaatgtgca ctagattccg atgctgactt gctgggtatt atatgtgtgc ccaatagaaa
     4801 gagaacaatt gacccggtta ttgcaaggaa aatttcaagt cttgtaaaag catataaaaa
     4861 tagttcaggc actccgaaat acttggttgg cgtgtttcgt aatcaaccta aggaggatg
     4921 tttggctctg gtcaatgatt acggcattga tatcgtccaa ctgcatggag atgagtcgtg
     4981 gcaagaatac caagagttcc tcggtttgcc agttattaaa agactcgtat ttccaaaaga
     5041 ctgcaacata ctactcagtg cagcttcaca gaaacctcat tcgtttattc ccttgtttga
     5101 ttcagaagca ggtgggacag gtgaactttt ggattggaac tcgatttctg actgggttgg
     5161 aaggcaagag agccccgaga gcttacattt tatgttagct ggtggactga cgccagaaaa
     5221 tgttggtgat gcgcttagat taaatggcgt tattggtgtt gatgtaagcg gaggtgtgga
     5281 gacaaatggt gtaaaagact ctaacaaaat agcaaatttc gtcaaaaatg ctaagaaata
     5341 ggttattact gagtagtatt tatttaagta ttgtttgtgc acttgcctgc aagccttttg
     5401 aaaagcaagc ataaaagatc aactgtaaaa tcaggtatct cgtagtccg
//


```





```


TAAAATCTCGTAAAGGAACTGTCTGCTCTG s3



TAAAATCTCGTAAAGGAACTGTCTGCTCTGtataaaaataggcgtatcacg 1804_TRP1fp_pTA replaces 1348 & 1680
                              --------------------- YEplac112 YCplac22 YIplac204


               GAACTGTCTGCTCTGttcaagaattaattcggtcg  1680_TRP1fp_pTA New TRP1 primer, partial s3, replaces 1348, replaced by 1804
                                        ----------  YXplacs snapgene


TAAAATCTCGTAAAGGAACTGTCTGCTCTGtttgccgattaagaattcg   1348_TRP1fp_pTA  This primer was replaced by 1680
                              -------------------   TRP1 SGD
                                           ------   YXplacs snapgene


tataaaaataggcgtatcacgaggccctttcgtcttcaagaattaattcggtcgaaaaaagaaaaggagagggccaagagggagggcattggtgactattgagcacgtgagtatacgtgattaagcacacaaaggcagcttggagtatg TRP1 YEplac112 YCplac22
--------------------- 1804        -------------------- 1680
                                            ------     1348

tataaaaataggcgtatcacgaggcc==================aattcggtcgaaaaaagaaaaggagagggccaagagggagggcattggtgactattgagcacgtgagtatacgtgattaagcacacaaaggcagcttggagtatg TRP1 YIplac204
--------------------- 1804                  ---------- 1680
                                            ------     1348

                               TTTGCCGATTAAGaattcggtcgaaaaaagaaaaggagagggccaagagggagggcattggtgactattgagcacgtgagtatacgtgattaagcacacaaaggcagcttggagtATG TRP1 SGD
                               ------------------- 1348

```

The YEplac112, YCplac22 and YIplac204 vectors all express the TRP1 gene. The sequences for these vectors are available from both Genbank and Snapgene
(see [[pTAx assembly strategy]]).

A peculiarity is that the YIplac204 TRP1 promoter seems to have an 18 bp deletion (marked by `==================`) compared to the sequences in YEplac112 YCplac22.
