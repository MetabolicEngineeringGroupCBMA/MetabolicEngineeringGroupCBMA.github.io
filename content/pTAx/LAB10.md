### Plasmid miniprep with commercial kit & restriction digestion

![[pTAx/EGB25_001-2.png|188x100]]

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

Preparation of  plasmids  using a commercial alkaline lysis mini prep kit. The teacher has prepared _E. coli_ cultures in liquid medium beforehand. Cultures with each plasmid were grown in or on [[LB]] with [[antibiotics]] for selection of the plasmids. We will use the  [[MB010_NZYMiniprep.pdf|NZYMiniprep]].

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
- When the gel run is completed, the teacher with take a picture using a [[GenoSmart|transilluminator]].

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

## Theoretical plasmid assembled by students on LAB5

![[pTAx/LAB10-1.png]]

## Annotated nanopore whole plasmid sequencing result

![[pTAx/LAB10.png]]

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

tataaaaataggcgtatcacgaggccxxxxxxxxxxxxxxxxxxaattcggtcgaaaaaagaaaaggagagggccaagagggagggcattggtgactattgagcacgtgagtatacgtgattaagcacacaaaggcagcttggagtatg TRP1 YIplac204
--------------------- 1804                  ---------- 1680
                                            ------     1348

                               TTTGCCGATTAAGaattcggtcgaaaaaagaaaaggagagggccaagagggagggcattggtgactattgagcacgtgagtatacgtgattaagcacacaaaggcagcttggagtATG TRP1 SGD
                               ------------------- 1348

```

The YEplac112, YCplac22 and YIplac204 vectors all express the TRP1 gene. The sequences for these vectors are available from both Genbank and Snapgene
(see [[pTAx assembly strategy]]).

A peculiarity is that the YIplac204 TRP1 promoter seems to have an 18 bp deletion (marked by `xxxxxxxxxxxxxxxxxx`) compared to the sequences in YEplac112 YCplac22.
