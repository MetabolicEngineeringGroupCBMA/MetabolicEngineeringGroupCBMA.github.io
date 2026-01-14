## In-vivo assembly of pTA cloning vectors in _Saccharomyces cerevisiae_

The MEC group has developed a protocol for the assembly of large metabolic pathways in-vivo.
This method is called the [Yeast Pathway Kit](https://pubmed.ncbi.nlm.nih.gov/26916955).

Briefly, single genes are cloned between a promoter and a terminator by in-vivo homologous recombination.
Metabolic pathways are built by linking single gene expression cassettes together in a second assembly step.

In the original publication, a plasmid called pYPKpw was used in order to facilitate maintenance of a
gene expression cassette or a pathway in _Saccharomyces cerevisiae_ or _E. coli_.

- amp (selection marker for E. coli)
- pUC (origin of replication for E. coli)
- 2µ  (origin of replication for _S. cerevisiae_)
- URA3 (selection marker for for _S. cerevisiae_
- ΔCRP (a partial, inactive E. coli cyclic AMP receptor protein (CRP) gene)

The CRP gene is inactive and only provide specific sequences for recombination.

It would be of interest to expand the range of plasmids for hosting single gene expression cassettes or pathways.

1. Having more selection marker for for _S. cerevisiae_ would make it possible to combine several
genes or pathways in the same cell.
2. The 2µ ori gives a relatively high copy number of the vector. Having
lower copy number would make it possible to fine tune gne expression
3. The pUC origin of replication results in a high copy number of the vector in E. coli. This
may lead to genetic instability in E. coli.
4. Making vectors out of standardized parts would make it possible to make new vectors simply by exchanging one part.


#### primer design for pTA1

Five PCR products were made with PCR primers that incorporate flanking sequences on each PCR product:

| PCR product 	| Template  	| Left side 	| Right side 	|
|-------------	|-----------	|-----------	|------------	|
| amp         	| pBR322    	| s5        	| s1         	|
| pBR         	| pBR322    	| s1        	| s2         	|
| LEU2        	| YEplac181 	| s2        	| s3         	|
| 2µ          	| YEplac112 	| s3        	| s4         	|
| ΔCRP        	| pYPKpw    	| s4        	| s5         	|

The actual sequences of s1 - s5 were 30 bp sequences designed
with the [R2oDNA designer](https://pubmed.ncbi.nlm.nih.gov/24933158) tool:

| Designation 	| Sequence                       	|
|-------------	|--------------------------------	|
| s1          	| AATCCAATCAGCGTAAGGTGTAGACTTTCT 	|
| s2          	| ATCGTATCTGCTGCGTAAATAGTAGTCAAC 	|
| s3          	| TAAAATCTCGTAAAGGAACTGTCTGCTCTG 	|
| s4          	| AACTGTAAAATCAGGTATCTCGTAGTCCGT 	|
| s5          	| GAAAAGCGTTTACCTCGGAACTCTATTGTA 	|


The vector is assembled by homologous recombination between the s1-s5 sequences.

             s1
     -|amp|30
    |      \/
    |      /\       s2
    |      30|pbr|30
    |             \/
    |             /\       s3
    |             30|mu2|30
    |                    \/
    |                    /\       s4
    |                    30|leu|30
    |                           \/
    |                           /\       s5
    |                           30|crp|30
    |                                  \/
    |                                  /\
    |                                  30-
    |                                     |
     -------------------------------------

## pTA3 to pTA10

A series of eight new vectors were planned according to the table below.


| Name  	| ec_marker 	| ec_ori 	| sc_ori  	| sc_marker 	| rec  	|
|-------	|-----------	|--------	|---------	|-----------	|------	|
| pTA3  	| amp       	| pBR    	| TWOµ    	| HIS3      	| ΔCRP 	|
| pTA4  	| amp       	| pBR    	| CEN_ARS 	| HIS3      	| ΔCRP 	|
| pTA5  	| amp       	| pBR    	| TWOµ    	| KanMX4    	| ΔCRP 	|
| pTA6  	| amp       	| pBR    	| CEN_ARS 	| KanMX4    	| ΔCRP 	|
| pTA7  	| amp       	| pBR    	| TWOµ    	| TRP1      	| ΔCRP 	|
| pTA8  	| amp       	| pBR    	| CEN_ARS 	| TRP1      	| ΔCRP 	|
| pTA9  	| amp       	| pBR    	| TWOµ    	| URA3      	| ΔCRP 	|
| pTA10 	| amp       	| pBR    	| CEN_ARS 	| URA3      	| ΔCRP 	|

Most fragments are similar to the pTA1 except for new primers for the Saccharomyces cerevisiae
markers (column "sc_marker") and the CEN/ARS yeast origin of replication.

More details [here](https://docs.google.com/spreadsheets/d/1OdQ8cHiCPM4s99EOmUx92wqeGYuMuN-x3YVP86VNloo/edit?usp=sharing)


### Class 1 Oct 13 / Oct 20 2020

Students have two main tasks:

- each student will make a plasmid DNA preparation by the alkaline lysis method
- each group will make solid medium to be used for the yeast transformation in Class 3

[[alkaline lysis plasmid mini prep\|Plasmid preparation]]

[[YPD\|YPD medium]]

[[SD\|SD medium]]


Material (Por turma, 2 turmas por dia, 2 dias):

1. Pipetas P1000, P100, P20 e P10
2. Pontas amarelas, azuis e brancas estéreis
3. Eppendorfs 1.5 mL *Novos*
4. Espátulas para pesar meios
5. 8 x Frascos Erlenmeyer 250 mL
6. 4 x Provetas graduadas 250 mL
7. Peptona
8. Extrato de levedura
9. Glucose
10. YNB Yeast Nitrogen Base
11. Agar
12. papel aluminio
13. fita cola para autoclavar
14. Barquinhos de pesagem
15. Marcadores
16. 4 caixas de esferovite para gelo
17. 4 tubos eppendorf com 1 mL tampão P1 (16 tubos no total)
18. 4 tubos eppendorf com 1 mL tampão P2  --"--
19. 4 tubos eppendorf com 1 mL tampão P3  --"--
20. 4 tubos eppendorf com 1 mL etanol seco 99% (qualidade pura para DNA)
21. 4 tubos eppendorf com 1 mL etanol 70% (qualidade pura para DNA)
22. 4 tubos eppendorf com 1 mL tampão TE

Não e preciso preparar P1, P2 ou P3, temos estas tampoes no LGM.



### Class 2 Oct 27 / Nov 03 2020

This practical class consists of two to three separate tasks.

1. Preparation of a PCR reaction.
2. Prepare an agarose gel for next class.
3. Repetition of medium preparation for some groups.

#### Preparation of a PCR reaction.

Each student should prepare two PCR reactions. One reaction to amplify a plasmid
part and one negative control. The difference between the amplification and
control is that the control has lower volume and no template DNA. All PCR components
need to be on ice at all times. Each group has an ice box with each of the four ingredients
 for PCR. **Pipette very carefully, there is only a limited amount of reagents.**

Put two PCR tubes on ice to cool down. Add the reagents in the order given below.

*PCR amplification (50µL):*
- 33 µL [[2x PCR mastermix\|MM2]] + [[6x DNA loading buffer\|LBx6]] (green)
- 5 µL primer 1 (1 mM)
- 5 µL primer 2 (1 mM)

*PCR control (20µL):*
- 13 µL MM2 + LBx6 (green)
- 2 µL primer 1 (1 mM)
- 2 µL primer 2 (1 mM)
- 3 µL ultrapure water

**Keep all tubes on ice at all time.**

The MM2 + LBx6 solution contain 2x concentrated PCR master mix and 6x
concentrated DNA loading buffer. This mixture contain all components needed
for PCR except primers and template. It also contain coloring and ficoll that
makes it easier to load the sample on a gel for analysis. The coloring and ficoll are
compatible with the PCR reaction. When you have prepared the tubes as described above,
leave them on ice.

#### Dilution of plasmid DNA

1. Unfreeze your plasmid DNA from Class 1.
2. Pipette 1000 µL ultrapure water into a fresh eppendorf tube
3. Mark this tube well so that you can identify it.
4. Put the tube on ice.
5. Vortex the tube with plasmid DNA so that you are sure that all DNA was dissolved.
6. Transfer 5 µL of the plasmid DNA to the tube with 1 mL water This will make a 5µL/1000µL = x200 dilution.
7. Vortex the tube with the x200 plasmid dilution so that the content is well mixed.
8. Put the plasmid DNA from Class 1 back into the freezer.
9. Transfer 7 µL of the x200 diluted plasmid to the tube with *PCR amplification (50µL)*.
10. Save both PCR tube in the freezer. Be sure to give each PCR tube a number according to the spreadsheet.

#### Prepare an agarose gel for next class

1. Weigh up 0.5 g agarose in a piece of paper or aluminium foil
2. Add 50 mL of 1x TAE or TBE buffer in a 100 mL Erlenmeyer flask
3. Add the agarose to the buffer and swirl the flask to mix
4. Run the flask for 30s in a microwave oven
5. Swirl the flask to mix and return to 4 if you can see undissolved agarose
6. Let cool until you can hold the flask in your hand. Continue to step 7.
7. Seal a gel tray with masking tape
8. pour the liquid gel in the tray
9. put a gel comb in place
10. Wait until the gel is solid, remove the gel and put it in a container with enough buffer to cover the gel

#### SD medium preparation (only for the groups that confused Yeast extract and Yeast Nitrogen Base)

1. Do the calculations to prepare 100 mL of medium with the following concentrations:

- 6.7 g/L YNB without amino acids (a.a.) **do not confuse with Yeast Extract**
- 20 g/L Glucose
- 20 g/L agar

2. Measure 100 mL of deionized water with a beaker, add a portion to the 200 mL bottle
3. Add all the ingredients and dissolve; add the remaining water
4. Identify the bottle with your group number and the name of the medium

Material:
- 100 mL Agua ultrapura estéril
- Pipetas P1000, P100, P20 e P10
- Pontas amarelas, azuis e brancas estéreis
- Tubos PCR
- Tubos Eppendorf *novos*
- Espátulas para pesar agarose
- Agarose
- ~500 de TAE buffer 1x
- 8x Provetas de 50 mL  e 100 mL
- 8x Frascos de 100 ou 250 mL
- 8x Suportes para géis de electroforesis
- Microondas
- Luvas para pegar frascos quentes
- 40x placas de Petri
- 2x Caixas escura para guardar geis de agarose
- 8x Frascos de 250 mL
- YNB without amino acids (a.a.)
- Glucose
- agar






### Class 3 Nov 10 / Nov 17 2020

This class has two main objectives, transformation of yeast and agarose gel electrophoresis of DNA.


#### Yeast transformation

Put one 1.5 mL Eppendorf tube for each student on ice and one extra for the group (4 tubes for a group with 3 members).
Each student should make one transformation and each groupsshould make one negative control transformation.

1. Add about 1/2 mL glass spheres to a to a petri dish with the appropriate solid medium for selection.
2. Transfer 1 mL ultrapure water to an empty Eppendorf tube and put the tube om ice. Cold water is needed later in the protocol.
3. Transfer 50 µL of the cell suspension to **empty** tubes. **Keep the tubes on ice when you are not pipetting**.
4. Spin the cells for 30 s at the highest speed.
5. Remove supernatant with a P200 pipette. Leave the cell pellet at the bottom of the tube.
6. Add 300 µL [[PEG LiAc ssDNA\|PLS]] to each cell pellet. **Keep the tubes on ice when you are not pipetting**.
7. Add 60 µL of the *DNA mix* (see below) or water (negative control) or plasmid (positive control).
8. Vortex the tubes until the cells are well resuspended.
9. Put the tubes in a floating tube rack at 42C
10. Incubate for 40 min (During this time you should load the agarose gel, see below).
11. Remove tubes and put on ice for 2 min
12. Spin tubes for 1 min at highest speed.
13. remove supernatant with a P1000 pipette. Leave the cell pellet at the bottom of the tube.
14. Add 300 µL cold water (from the tube on ice, step 2) and resuspend with the pipette.
15. Transfer 200 µL of the cell suspension to the petri dish with the solid medium
16. Spread the cells by shaking (The samba method).


#### Preparation of DNA mix

- PCR products from Class 2  were pooled and diluted with water.
- Add together 12 µL of each DNA fragment according to the Google https://docs.google.com/spreadsheets/d/1OdQ8cHiCPM4s99EOmUx92wqeGYuMuN-x3YVP86VNloo/edit#gid=1577554029


#### Agarose gel electrophoresis of DNA

Each student has three types of DNA, plasmid DNA from Class 1 and two PCR reaction (+/-) from Class 2.

- Unfreeze the plasmid DNA if this was not already done.
- Add 17 µL of water to an Eppendorf tube
- Add  5 µL 6xloading buffer [[6x DNA loading buffer\|LBx6]].
- Add  8 µL plasmid DNA.
- If necessary, spin the tube for ~5 seconds to collect the liquid at the bottom.
- Put the gel in the electrophoresis chamber.
- Add more buffer until the gel is just submerged.
- Add 10 µL of the mixture above from left to right : `Plasmid DNA with loading buffer|PCR reaction (+)|PCR control (-)`.
- Apply the electrical field as soon as you are done.
- The electrophoresis last around 15 - 30 min at 100 volts in the [[Bio Rad Mini Sub Cell]].

#### Post stain

- Put the gel in TAE + Midori, incubate 15-30 min
- Take picture


Material:
- Pipetas P1000, P100, P20 e P10
- Pontas amarelas, azuis e brancas estéreis
- Tubos Eppendorf **novos**
- ~500 ml de TAE buffer 1x
- sistema de electroforese
- 4 caixas de esferovite para gelo
- esferas de vidro estereis
- 4 barcos para tubos eppendorf


### Class 4 2020-11-24 | 2020-12-15

The main objective of this class is to do a plasmid rescue from yeast to E. coli.
This consists of a plasmid extraction from _S. cerevisiae_ followed by transformation of _E. coli_.


#### Plasmid extraction from _S. cerevisiae_ using alkaline lysis

This protocol allow the isolation of small quantities of plasmid DNA from Saccharomyces cerevisiae for the
subsequent transformation of E. coli (i.e. plasmid rescue).

1. Transfer ~5 mL of yeast culture to a 5 mL Eppendorf tube.

2. Spin the tubes in a centrifuge for 1 min at 5000 rpm.

3. Remove supernatant by decanting and add 1 mL ultra-pure water.

4. Vortex to resuspend the cells.

5. Transfer the cell suspension to a 2 mL Eppendorf tube, discard the 5 mL tube.

6. Spin the 2 mL tube with cells for 30s in a microcentrifuge.

7. Remove supernatant by decanting.

8. Add 200 µL P1 buffer.

9. Add 200 µL of glass beads (about one 0.2 mL PCR tube of beads).

10. Vortex the tubes for 3 minutes using the [[disruptor genie]]. Go to step **11** as soon as possible.

11. **Wear goggles for this step!** Put the tube on ice. Add 200 µL of  buffer P2 as soon as possible, mix by inversion
about ten times, **do not vortex** or else the chromosomal DNA might fragment and contaminate the plasmid DNA.
The disruption of the cells liberate nucleases that can destroy the DNA. **Incubate for a maximum of five minutes.**

12. Add 200 µL buffer P3, mix by inversion about ten times

13. Centrifuge at top speed for 5 min.

15. While centrifuge is running, add 1 ml of 96% - 99,5% ethanol to a new clean 1.5 ml Eppendorf tube.

16. Transfer up to 500 µL of the supernatant from the centrifugation to the tube with ethanol and mix by inversion.
Be careful not to transfer any of the white precipitate.

17. Centrifuge at top speed for 5 or 10 min.

18. Remove supernatant by opening and inverting the tube.
The plasmid may be visible as a small white spot in the bottom of the tube.

19. Add 1 mL 70% ethanol.

20. Centrifuge 1 min at top speed.

21. Remove supernatant by opening and inverting the tube.

22. Remove all liquid by pipetting with a P20, P100 or P200 pipette. Do not touch the DNA pellet.

23. Dry the DNA at 50°C for 5 min with the lid open.

24. Add 50 µL TE buffer to the DNA, vortex to dissolve.

25. Put the tube with DNA on ice.


### Transformation of _E. coli_

These cells were prepared according to the [[SEM (Inoue) competent cells\|SEM]] protocol.

The competent cells are **very sensitive to heat**. Do not let them warm up, or they will lose their efficiency.
Keep them on ice as much as possible.

1. Get one tube of 50 µL competent cells for each transformation.

2. Add 5 µL DNA to each tube, flick the tube to mix.
Do **NOT** vortex the cells at this point.

3. Incubate on ice for 10 min.

4. Heat shock in water bath at 42°C during **EXACTLY** 45s

5. Incubate for 1 min in a water/ice slurry for fast heat transfer. It is important that the cells cool down fast.

6. Add 1 mL [[SOC]] medium heated to 37°CC

7. Incubate at 37°C for 20 min

8. Centrifuge the cells for 30 s

9. Remove 900 µL of the supernatant with a pipette. Resuspend the cells with the remaining liquid.

10. Add all of the cell suspension to an LB-amp plate with 5-15 sterile glass beads and swirl to spread the liquid.

11. Incubate plates inverted at 37°C over-night. No parafilm is needed.

















[[Yeast genomic DNA extraction with LiOAc SDS]]

1. Pick a sufficient quantity of yeast cells from the plate or spin down 200 μL liquid yeast culture (OD600 ~ 0.4).
2. Suspend cells in 100 μL LiOAc (200 mM) with 1% SDS.
3. Incubate for 5-15 min at 70°C. We float the tubes in recently boiled water.
4. Add 300 μL 96–100% ethanol, then mix by brief vortexing.
5. Spin down DNA and cell debris at 15,000×g or the maximum speed that the microcentrifuge allow for 3 min.


6. Remove supernatant by decanting or pipetting.
7. Add 1 mL 70% ethanol. Vortex briefly.
8. Spin at the maximum speed that the centrifuge allow for 30s.
9. Remove ethanol by decanting or pipetting.
10. Dissolve pellet in 100 μL [[TE]], H2O or Elution buffer from a miniprep kit.
11. Spin down cell debris for 15 s or more at maximum speed.
12. Use 1 μL supernatant for PCR.
13. Store the chromosomal DNA at -20°C if it is not to be used immediately.






Agarose
TAE buffer
4x Frascos Erlenmayer 100 ou 250 mL
4x Suportes para géis de electroforese
Loading buffer
Marcador de pesos moleculares
Midori ou outro marcador de DNA
Sistema de electrophorese

Oct 27
Nov 03

Oct Preparation of Taq DNA Polymerase from E. Coli
Pipetas P1000, P100, P20 e P10
Pontas amarelas, azuis e brancas
Eppendorfs
dNTPs
Tubos PCR
Termo-bloco ou banho 75°C
Água ultrapura – 50 mL
TEN buffer (10 mM Tris-HCl pH 7.9; 1 mM EDTA; 100 mM NaCl)

Nov 11
Nov 17

Oct-22 – PCR reaction/ Preparation of agarose gels
Pipetas P1000, P100, P20 e P10
Pontas amarelas, azuis e brancas
Tubos PCR
Espátulas para pesar agarose
Agarose
TAE buffer
4x Frascos Erlenmayer 100 ou 250 mL
4x Suportes para géis de electroforese
Loading buffer
Marcador de pesos moleculares
Midori ou outro marcador de DNA
Sistema de electrophorese

Nov 24
Dec 15

Oct-29 – Ligation (Plasmid + PCR Products) & Bacterial Transformation (Prof Bjorn)
Pipetas P1000, P100, P20 e P10
Pontas amarelas, azuis e brancas
Eppendorfs
lamparinas
Incubadora e banho a 37 °C

Nov-5 – Yeast Transformation
Pipetas P1000, P100, P20 e P10
Pontas amarelas, azuis e brancas
Eppendorfs
lamparinas
Termo-bloco
Banho
Água autoclavada 1L
Acetato de lítio 1M
PEG 50%
ssDNA
espalhadores

Nov-12– CRISPR

Nov-19 – Mathematics & English in the laboratory

Nov-26 – JORNADAS DE ENGENHARIA BIOLÓGICA

Dec-03 – Measuring Lactase Enzymatic Activity
Pipetas P1000, P100, P20 e P10
Pontas amarelas, azuis e brancas
Eppendorfs
Almofariz
Cuvetes
PBS
4 banhos a 37 °C

Dec-10 – Q&A

Dec-17- TEST
