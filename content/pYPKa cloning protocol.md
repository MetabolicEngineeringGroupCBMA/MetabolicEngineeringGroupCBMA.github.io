The pYPKa vector is a [positive selection vector](https://www.tandfonline.com/doi/abs/10.1080/07388550290789504) for rapid cloning in *E. coli*.
It is a derivative of the [pCAPs](https://pubmed.ncbi.nlm.nih.gov/9514792) vector.
The pYPKa vector is lethal in most *E. coli* strains unless a fragment is cloned so that the toxic `crpS` gene in pYPKa is disrupted.
The advantage of this vector is that PCR products can be cloned without purification or digestion with restriction enzymes.

It is easy to use, once you have learned to work with it. See the end of this page for trouble shooting.

The first step is to prepare the pYPKa vector. This cloning procedure is sensitive to nuclease contamination. The reason for this is that the vector loses its toxicity if it is not intact and this could facilitate the formation of empty clones.

> [!WARNING]
> Do not add phosphatase (such as SAP or FastAP for example) to the digestion. 5' phosphates on the vector are necessary to form a partial bond with the PCR produc

Care should be taken to avoid nuclease contamination and leave as little time as possible for nucleases to act.
Use a standard commercial miniprep kit to prepare the plasmid if available. The [NZYMiniprep](https://www.nzytech.com/en/mb010-nzyminiprep) works very well for this purpose in our hands.

![[pYPKa cloning protocol-20240710075733703.png]]

Use the clone in the *E. coli* [DHM1](https://journals.asm.org/doi/10.1128/jb.187.7.2233-2243.2005) background (µ378 or µ379) as this has an *recA1 endA* genotype which improves plasmid stability and quality..

Use an optional wash step for nuclease removal if your kit includes one. Optionally, **heat the eluted plasmid solution to 80°C for 20 minutes** in order to remove all traces of nuclease.

The plasmid yield is normally quite low. This is not a problem as the protocol gives plenty of transformants with our homemade [[SEM (Inoue) competent cells]].

#### Digestion using [ZraI](https://www.neb.com/products/r0659-zrai#Product%20Information), [AjiI](https://www.thermofisher.com/order/catalog/product/ER1941) or [EcoRV/Eco32I](https://www.thermofisher.com/order/catalog/product/ER0301)

The digestion below is enough for ten ligations. It can be scaled up or down as required.
It is probably **not** necessary to add more enzyme even for a larger digestion.
It also probably better **not** to make prolonged digestions as this might increase the risk
for damaging the vector. The example below is for AjiI, but the principle is the same for ZraI
or EcoRV digestion:

**pYPKa vector digestion:**

| Table#1 | Vol (µL) | Component      |
| ------- | -------- | -------------- |
|         | 5.5      | ddH2O          |
|         | 3        | pYPKa miniprep |
|         | 1        | 1X Buffer AjiI |
|         | 0.5      | AjiI (5U/µL)   |

Incubate  15 - 30 min at 37°C. If your final construct does **not** have AjiI sites, inactivation is unnecessary, else inactivate AjiI by incubation at 65°C for 20 min.

It is practical to do the above digestion/inactivation in a PCR thermal cycler in available. Put the digestion on ice **immediately** after the digestion has finished.

The digested vector can be stored at -20°C at this point. Repeated freeze thaws should probably be avoided, due to the risk for damaging the DNA ends that could result in higher background.

A typical ligation (10 µL) with pYPKa is:

| Table#2 | ligation w 5x buffer | vol (µL) | Component                                              |
| ------- | -------------------- | -------- | ------------------------------------------------------ |
|         |                      | 5.5      | insert PCR product (**or** water for negative control) |
|         |                      | 1        | water                                                  |
|         |                      | 1        | **pYPKa vector digestion**                             |
|         |                      | 2        | 5x [[Ligase buffer]]                                   |
|         |                      | 0.5      | T4 DNA ligase enzyme                                   |
|         | total                | 10       |                                                        |
We routinely use the T4 DNA ligase from [thermofisher](https://www.thermofisher.com/order/catalog/product/EL0011). Our homemade ligase buffer is 5x concentrated has [PEG](https://bitesizebio.com/44754/faster-ligations-peging-down-the-secret) included and works very well. Some commercial buffers are 10 x concentrated and they come with or without PEG.

| Table#3 | ligation w 10x buffer | vol (µL) | Component                                                                   |
| ------- | --------------------- | -------- | --------------------------------------------------------------------------- |
|         |                       | 5.5      | insert PCR product (**or** water for negative control)                      |
|         |                       | 1        | water                                                                       |
|         |                       | 1        | 50% (w/v) polyethylene glycol 4000 or similar                               |
|         |                       | 1        | **pYPKa vector digestion**                                                  |
|         |                       | 1        | 10x [Ligase buffer](https://www.thermofisher.com/order/catalog/product/B69) |
|         |                       | 0.5      | T4 DNA ligase enzyme                                                        |
|         | total                 | 10       |                                                                             |





Since the mix has so many components, it is practical to mix buffer, water and enzyme together in a Ligation mix (LM).

#### Ligation mix (LM)

Use a ligation buffer containing PEG or add PEG as per the ligase manufacturers instructions. The [[Ligase buffer\|homemade ligase buffer]] works very well.
Mix the following on ice in the indicated order for EACH ligation reaction:

**LM**

- 1 µL water or acetylated BSA (10 mg/ml, BSA can help [speed up ligation](http://se.promega.com/resources/pubhub/enotes/shorten-the-ligation-time-for-the-pgem-t-vector-systems/))
- 2 µL 5x [[Ligase buffer\|LIGATION buffer]]
- 0.5 µL T4 DNA ligase (5 U/µL) (Keep on **ice** until use).

Thus, for ten reactions (with 10 % extra volume margin) the ligation mix will be:

- 11 µL water
- 22 µL 5x LIGATION buffer
- 5.5 µL ligase (1 U/µL)

mix by vortexing briefly. Keep on **ice** until use.

Ligation simplifies to:

- 5.5 µL insert PCR product (or water for negative control)
- 1 µL **pYPKa vector digestion**
- 3.5 µL Ligation mix (**LM**)

Ligation at 37°C for one hour or in the fridge overnight or over a weekend seems to work well. Ligation at 37°C for ~15 min is used in many protocols.

> [!WARNING]
> Do *not* heat inactivate the ligase prior to transformation. Heat inactivation of PEG-containing reactions will cause your transformations to fail.

 The ligation mix can be transformed right away or stored in fridge or freezer.

### Transformation

We usually transform with all of the mixture (10 µL) using [[Transforming Frozen Competent E. coli\|this]] protocol. We use prewarmed (37°C) LB medium for recover (1h) and prewarmed LB plates for plating.
We add the ampicillin to the cells before plating.
### Colony Picking and Colony PCR

A successful cloning should have (far) fewer colonies on the negative control plate (ligation with water) than on the ligation with insert. Click on the image for a larger picture.

[![[pYPKa_cloning_small.png]]](pYPKa_cloning_large.jpg)

Analyzing 10-12 clones should be sufficient to identify several positive clones.

### Checking insert presence and direction by PCR

The fastest way to check the insert presence and orientation is by colony PCR. The primer sets below all flank the the cloning sites. The 468 primer has a high melting temperature and can be substituted for 1715 if this is deemed a problem. Using three primers facilitate the formation of a PCR product even when the plasmid is empty.

| Table#4 | #   | Primer1          | Primer2          | Primer3 | Orientation A (bp) | Orientation B (bp) | empty vector (bp) | Comment                                             |
| ------- | :-- | :--------------- | ---------------- | ------- | ------------------ | ------------------ | ----------------- | --------------------------------------------------- |
|         | 1   | 468              | 467              | -       | 50 + 37 + insert   | 50 + 37 + insert   | 87 (❗)            | Detect any insert, does not give cloning direction. |
|         | 2   | 468              | insert rv primer | -       | 50 + insert        | ∅                  | None              | Only gives a product for one orientation            |
|         | 3   | insert fw primer | 467              | -       | 37 + insert        | ∅                  | None              | Only gives a product for one orientation            |
|         | 4   | 468              | insert fw primer | 578     | 50 + insert        | 326 + insert       | 376 (❗)           | Shorter fragment for Orientation A                  |
|         | 5   | 577              | insert rv primer | 467     | 218 + insert       | 37 + insert        | 255 (❗)           | Shorter fragment for Orientation B                  |
|         | 6   | 1807             | insert fw primer | 467     | 378 + insert       | 37 + insert        | 415               | Shorter fragment for Orientation B                  |

(❗) Note that these fragment are always expected from colony PCR and other situations where E. coli chromosomal DNA is present due to the presence of the CRP gene.

```


>577_crp585-557 (29-mer)
gttctgatcctcgagcatcttaagaattc

>467_pCAPs_release_re (31-mer)
ATTTAAatcctgatgcgtttgtctgcacaga

>468_pCAPs_release_fw (25-mer) 79.66 same as 560
gtcgaggaacgccaggttgcccac

>1715_pCAPs_release_fw shorter version of 468 (19-mer)
gtcgaggaacgccaggttg

>578_crp42-70 (29-mer)
gttcttgtctcattgccacattcataag

>1807_fw_pYPKa primer to check insert orientation
gtgataAATCAGTCTGCGCCACATCG

```

Primers binding to the pYPKa are available [here](standard_primers).

### Common mistakes or errors

| Symptom                              | Problem                                    | Remedy                                                       |
| ------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| Lots of colonies in negative control | too much vector in the ligation            | Use less vector                                              |
| "                                    | nuclease contamination in the plasmid prep | Prepare new plasmid DNA, heat treat to inactivate nucleases. |
| "                                    | PCR carry-over                             | Gel purify or perform PCR with less template DNA.            |
| No colonies                          | cells not competent enough                 | Use more vector or preferrably cells with higher competency  |
| "                                    | Alkaline phosphatase                       | Leave out phosphatase                                        |
|                                      |                                            |                                                              |

Expect four out of five clones with insert, perhaps five out of ten for long or difficult inserts. **Make sure to include a negative ligation control, at least in the beginning of adopting the pYPKa cloning protocol**. This control is made by excluding the insert and replacing it with water.

If the insert is a PCR product that originated from an *E. coli* plasmid with ampicillin marker, there is a risk of carry over plasmid contamination from the PCR product. Avoid this by using very little template in your PCRs or including a control with insert but without linear pYPKa. Check this by transformation with insert only. There is also plasmid contamination (ampicillin resistance) in our homemade Taq polymerase.

Learn more about ligation [[ligation\|here]].
