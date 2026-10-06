---
publish: true
---

# UC Genética e Biotecnologia Molecular 26-27 / Metabolic Engineering

![[GBM26if03iw.png]]
Figure from [Keasling, J. D. 2010](https://doi.org/10.1126/science.1193990)

This document contains notes and links for the Metabolic Engineering lecture and practical class for the
course Genética e Biotecnologia Molecular, taught to students in Mestrado em Bioquímica Aplicada (MBQA)
or Mestrado em Genética Molecular (MGM).

# Lecture

You can see the lecture slides on Blackboard. See the [[ethanol from wood]] problem solution.

## TP exercise class

![[banana_oil.png]]

You need to bring a **laptop** computer to this class, and you also need the [[ApE]] plasmid editor app.

Your task is to assemble the sequence of the ATF1 expression vector `pTA1_TDH3_ScATF1_PGI1` using the Yeast Pathway Kit.

## 1. Assembly of the pYPKa\_A\_ScATF1 vector

Your first task is to assemble the pYPKa\_A\_ScATF1 vector. Follow [[in silico assembly of pYPKa_A_ScATF1|these]] instructions. When you have your result, calculate the SEGUID checksum by using the fingerprint button in [[ApE]]. Compare your result with that of your instructor and your colleagues.

## 2. Assembly of the pTA1\_TDH3\_ScATF1\_PGI1 vector

Your second task is to assemble the pTA1\_TDH3\_ScATF1\_PGI1 vector. You need the pYPKa\_A\_ScATF1 plasmid sequence that you assembled in the previous task. Follow these [[in silico assembly of pTA1_TDH3_ScATF1_PGI1|instructions]].

## Practical class

We will perform an [[alkaline lysis plasmid mini prep]] from yeast followed by an [[Transforming Frozen Competent E. coli|E. coli transformation]]. This combination is called a "[[plasmid rescue|Plasmid rescue]]".
This is done because plasmid DNA yield and purity are higher in _E. coli_. Purifying the DNA helps us verify that the plasmid is correct using DNA sequencing and other methods.

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
18. Label the tube with your number. Store the tube in the fridge or freezer (4 °C or -20 °C).

### _E. coli_ transformation

1. Add 10 µL of the plasmid DNA to the tube containing competent cells and flick the tube a few times to mix. Do **NOT** vortex the cells at this point.
2. Incubate for ==up to== 30 min on ice.
3. Heat shock in a water bath at 42 °C for **EXACTLY** 45 s.
4. Cool the tube for 1-2 min on ice or in a water/ice slurry for faster heat transfer.
5. Add 1 mL of pre-warmed liquid [[LB]] medium to the tube and proceed to the next step, or let the cells recover at **37 °C** for **1 h**.
6. Perform the colony PCR described below during the 1 h incubation.
7. Pipette 300 µL of the contents onto an LB plate with 10-20 sterile glass beads and swirl the plate to spread the liquid.
8. Incubate the plates inverted for 18-24 h at 37 °C.

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
9. Add **17 µL** of PCR mix<sup>\*</sup> to a new PCR tube (these are the small tubes).
10. Add **3 µL** of the yeast-NaOH mix to the PCR tube without disturbing the cell debris at the bottom of the tube.
11. Put the tubes in the PCR machine.
12. Run this PCR program:

```
>1748_s3 s3 tm=53.243
TAAAATCTCGTAAAGGAACT
>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC

|95°C |95°C               |    |tmf:51.3
|_____|_____          72°C|72°C|tmr:51.4
|10min|30s  \ 53.7°C _____|____|45s/kb
|     |      \______/ 1:15|5min|GC 40%
|     |       30s         |    |1667bp

```

<!--
alternative primer pair:
>1682_s3 pTAx
TAAAATCTCGTAAAGGAACTGTCTGCTCTG
>1742_s4r s4r tm=53.771
ACGGACTACGAGATAC
-->

Extra: How banana flavor is formed during whiskey fermentation ([article](https://www.linkedin.com/pulse/from-protein-banana-chemistry-behind-whiskys-fruitiness-john-angus-has8e/)).
