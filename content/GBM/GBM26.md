---
publish: true
---

# UC Genética e Biotecnologia Molecular 26-27 / Metabolic Engineering

![[GBM/GBM26if03iw.png]]
Figure from [Keasling, J. D. 2010](https://doi.org/10.1126/science.1193990)

This document contains notes and links for the Metabolic Engineering lecture and practical class for the course Genética e Biotecnologia Molecular, taught to students in Mestrado em Bioquímica Aplicada (MBQA) or Mestrado em Genética Molecular (MGM).

# Lecture

You can see the lecture slides on Blackboard after the class. See the [[ethanol from wood]] problem solution. The [[metabolic maps]] used in the theoretical class.

## TP exercise class

![[banana_oil.png]]

You need to bring a **laptop** computer to this class, and you also need the [[ApE]] plasmid editor app.

Your task is to assemble the sequence of the ATF1 expression vector`pTA1_TDH3_ScATF1_PGI1` _in-silico_ using [[The Yeast Pathway Kit]].

## 1. Assembly of the pYPKa\_A\_ScATF1 vector

Your first task is to assemble the pYPKa\_A\_ScATF1 vector. Follow [[in silico assembly of pYPKa_A_ScATF1|these]] instructions. When you have your result, calculate the SEGUID checksum by using the fingerprint button in [[ApE]]. Compare your result with that of your instructor and your colleagues.

## 2. Assembly of the pTA1\_TDH3\_ScATF1\_PGI1 vector

Your second task is to assemble the pTA1\_TDH3\_ScATF1\_PGI1 vector. You need the pYPKa\_A\_ScATF1 plasmid sequence that you assembled in the previous task. Follow these [[in silico assembly of pTA1_TDH3_ScATF1_PGI1|instructions]].

## Metabolism

[[Erlich pathway]]

## Practical class

We will perform an [[alkaline lysis plasmid mini prep]] from yeast followed by an [[Transforming Frozen Competent E. coli|E. coli transformation]]. This combination is called a "[[plasmid rescue|Plasmid rescue]]". This is done because plasmid DNA yield and purity are higher in _E. coli_. Purifying the DNA helps us verify that the plasmid is correct using DNA sequencing and other methods.

We will also prepare a diagnostic colony [[standard pcr protocol|PCR]] reaction to amplify a specific part of the plasmid. If we have time, we will separate the PCR product on an [[Agarose electrophoresis|agarose gel]] together with a molecular marker as an initial indication that the plasmid sequence has been assembled correctly.

### Plasmid rescue to _E. coli_

- Prepare crude yeast DNA from cells with glass beads and an _E. coli_ plasmid miniprep kit
- Transform _E. coli_ with crude yeast DNA
- Plate _E. coli_ on Petri dishes with solid LB-amp medium from LAB7

### Plasmid preparation from _S. cerevisiae_, one per group

1. Scrape some yeast cells off a plate.
2. Add **200** µL of **P1**.
3. Resuspend by vortexing.
4. Add 200 µL of glass beads (about one full 0.2 mL PCR tube).
5. Vortex the tubes for 5 min using a [[disruptor genie]].
6. Add **200** µL of P2 **as soon as possible**, as cell disruption releases nucleases that can damage the DNA.
7. Slowly invert the tube for ~4 min.
8. Add **==250==** µL of buffer P3 and mix by slowly inverting the tube at least ten times.
9. Centrifuge at top speed for **10** min.
10. Transfer ~500 µL of the supernatant to **1 mL of 100% ethanol** in a fresh tube and mix by inversion.
11. Centrifuge at top speed for **10** min. Make sure the hinge of the tube is facing outwards.
12. Pour away the supernatant. The plasmid DNA should be visible as a white spot.
13. Add **1 mL of 70% EtOH**. Mix by inverting the tube 2-3 times.
14. Centrifuge for **1** min at top speed.
15. Pour away the supernatant by opening and inverting the tube.
16. Evaporate the ethanol by opening the tube lid and leaving the tube at 50 °C for 5 min.
17. Resuspend the DNA pellet in 50 µL of 1x TE buffer.
18. Label the tube with your number. Store the tube on ice for now.

### _E. coli_ transformation

1. Add 10 µL of the plasmid DNA to the tube containing competent cells and flick the tube a few times to mix. Do **NOT** vortex the cells at this point.
2. Incubate for ==up to== 30 min on ice.
3. Heat shock in a water bath at 42 °C for **EXACTLY** 45 s.
4. Cool the tube for 1-2 min on ice or in a water/ice slurry for faster heat transfer.
5. Add 1 mL of pre-warmed liquid [[LB]] medium to the tube and proceed to the next step, or let the cells recover at **37 °C** for **1 h**.
6. Perform the **diagnostic PCR** described below during the 1 h incubation.
7. Pipette 300 µL of the contents onto an LB plate with 10-20 sterile glass beads and swirl the plate to spread the liquid.
8. Incubate the plates inverted for 18-24 h at 37 °C.

### Diagnostic PCR

1. Add 180 µL of TE buffer to a new 1.5 mL [[Eppendorf]] tube
2. Add 20 µL of you _S. cerevisiae_ plasmid DNA preparation
3. Mix by vortexing briefly.
4. Add **3 µL** of the diluted DNA to a PCR tube (these are the small tubes).
5. Your instructor will add **17 µL** of PCR mix<sup>\*</sup> to your tube.
6. Put the tubes in the PCR machine.
7. Run the PCR program below:

### Colony PCR

Summary:

- NaOH total yeast DNA preparation
- Colony PCR

#### NaOH Yeast DNA Preparation

Each student should have a plate with colonies. Do not contaminate this plate; we will need these yeast cells later.

![[pTAx/EGB24-20240311180844739.png]]

1. Watch this [YouTube](https://youtu.be/_aAQofQHnss) video (2 min) describing the technique.
2. Add 20 µL of 20 mM NaOH to a clean 1.5 mL Eppendorf tube.
3. Pick a small number of cells from your plate with a yellow pipette tip for transfer to the NaOH solution. **Do not take too many cells or any agar** (see 52 s in the video).
4. Add the cells to the solution and swirl to mix (see 59 s in the video).
5. Incubate the tubes at 95 °C for **ten** minutes.
6. When the 95 °C incubation is over, add 40 µL of [[TE]] buffer.
7. Vortex the tube for 3-5 s.
8. Spin at maximum speed in a microcentrifuge for 10-20 s.
9. Add **17 µL** of PCR mix (see below) to a new PCR tube (these are the small tubes).
10. Add **3 µL** of the yeast-NaOH mix to the PCR tube without disturbing the cell debris at the bottom of the tube.
11. Put the tubes in the PCR machine.
12. Run the PCR program below:

### PCR program and primers

```
|95°C |95°C               |    |tmf:51.3
|_____|_____          72°C|72°C|tmr:51.4
|10min|30s  \ 53.7°C _____|____|45s/kb
|     |      \______/ 1:15|5min|GC 40%
|     |       30s         |    |1667bp

Primers:

>1748_s3 s3 tm=53.243
TAAAATCTCGTAAAGGAACT
>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC
```

### PCR mix

| Component                                                          | µL  |
| ------------------------------------------------------------------ | --- |
| [[2x PCR mastermix]]                                               | 250 |
| [[6x DNA loading buffer\|6 x DNA loading buffer (PCR compatible)]] | 83  |
| Primer 1748 (10 µM)                                                | 50  |
| Primer 1742 (10 µM)                                                | 50  |
| Total                                                              | 500 |

<!-- alternative primer pair:
>1682_s3 pTAx
TAAAATCTCGTAAAGGAACTGTCTGCTCTG
>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC -->

### Extra reading

How banana flavor is formed during whiskey fermentation ([article](https://www.linkedin.com/pulse/from-protein-banana-chemistry-behind-whiskys-fruitiness-john-angus-has8e/)).

### Results (MBQA)

We seem to have colonies on about half of the plates from the _E. coli_ transformation. I will take picture tomorrow.

PCR Tubes collected during class:

![[GBM/GBM266hgo7z.jpg|585x441]]

I had to transfer 2,4 16,17,18,19 to new tubes as the PCR mix can evaporate if tubes of different sizes are used at the same time.

![[GBM/GBM261uvgc4.jpg|615x465]]

Program:

![[GBM/GBM268v04ye.jpg|543x410]]

Result: [[people|Luana]], MSc student in my group ran the gel for us (🙏) :

![[GBM/GBM26bswold.png]]
We have positive results for 1,3,11,12,13,15,16,17,19 (4, 9, 10 weak bends).

### Results (MGM)

![[GBM/GBM26gabsm0.png]]

![[GBM/GBM26d47nrg.png]]

![[GBM/GBM264u5o7r.png]]

![[GBM/GBM26reoklf.png]]

![[GBM/GBM26sq90xf.png]]

### Discussion

What do the positive results mean? I hope that the plasmid in the yeast cells is a plasmid called `pTA5_TDH3_ScATF1_PGI1`. This plasmid was made by the students of [[GBM24]] . They transformed a yeast strain carrying the `pTA1_TDH3_ScATF1_PGI1` plasmid (this is the one we assembled during the TP class) with the KanMX4 geneticin resistance marker. They got transformants, but these were never confirmed until today (Oct 7 2026).

Why would we want the `pTA5_TDH3_ScATF1_PGI1` plasmid? The geneticin marker can be used for selection in any yeast strain, the previous marker (LEU2) can only be used in a yeast mutant where this gene has been deleted or inactivated. This plasmid makes it possible to test other strain backgrounds such as wine or industrial strains.

### Photo album

[here](https://photos.app.goo.gl/Q7acvSpbPqGtHyMAA)

### Study questions

1. Why can a yeast with a fast initial production rate still perform poorly during repeated cell recycling?
2. How do product titre, yield and productivity differ?
3. How would you calculate the percentage of theoretical ethanol yield obtained from wood? Use the assumptions from the lecture.
4. Why can the XR/XDH xylose pathway create a cofactor imbalance and accumulate xylitol?
5. What problem does xylose isomerase avoid, and which downstream steps are still needed?
6. Why does reduced xylitol production not necessarily mean improved ethanol production?
7. How could limited pentose phosphate pathway capacity restrict xylose metabolism?
8. Which controls would help compare the same engineered pathway in laboratory and industrial yeast strains?
9. What does growth of an AccTet strain expressing heterologous ACC1 under tetracycline demonstrate?
10. How many NADPH molecules are consumed per fatty acid elongation cycle?
11. How can changes in lipid synthesis, storage or breakdown increase TAG accumulation?
12. Why does a change in relative fatty acid composition not establish increased total fatty acid production?
13. What reaction does Atf1 catalyse, and why might ATF1 overexpression fail to increase isoamyl acetate production?
14. What roles do the TDH3 promoter, ATF1 coding sequence and PGI1 terminator play in the expression vector?
15. Which fragments are needed to assemble the final expression vector, and why is checking plasmid length alone insufficient?
16. Why is KanMX4 useful when transferring the vector into a LEU2-functional industrial yeast?
17. Why rescue a yeast plasmid into E. coli, and which transformation controls help interpret an absence of colonies?
18. How does the practical’s DNA dilution change the amount of original preparation added to PCR? Why can dilution improve amplification?
19. What does an expected-size diagnostic PCR band establish? How would a band in the no-template control affect your interpretation?
20. How would you verify plasmid structure and maintenance, then test whether the engineered yeast produces more isoamyl acetate? Include suitable controls.
