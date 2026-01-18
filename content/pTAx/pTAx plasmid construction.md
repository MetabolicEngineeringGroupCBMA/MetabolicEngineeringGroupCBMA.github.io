
![[pTAx/EGB24-20240705161734646.jpeg]]

[original artwork](https://www.instagram.com/spettsart/?hl=en)

The objective of this lab course is to construct a new plasmid cloning vector in the pTAx series. This vector will be an *[E. coli](https://en.wikipedia.org/wiki/Escherichia_coli)* /  _[Saccharomyces cerevisiae](https://en.wikipedia.org/wiki/Saccharomyces_cerevisiae)_ [shuttle vector](https://en.wikipedia.org/wiki/Shuttle_vector). This vector will be useful for cloning genes and pathways using the Yeast Pathway Kit, see the next section "**Background**" "for more details.
### Background

In the [mec](https://metabolicengineeringgroupcbma.github.io/) research group, we are interested in understanding and engineering the biosynthesis of fatty acids and related products by the unicellular fungi known as baker's yeast [*S. cerevisiae*](https://en.wikipedia.org/wiki/Saccharomyces_cerevisiae).

![[pTAx/pTAx plasmid construction.png|540x304]]


Genetic engineering of complex traits often require the simultaneous deletion and/or expression of multiple genes. This is a challenging problem as genetic engineering is time consuming. To solve this problem, we developed a protocol for the parallel assembly of metabolic pathways that we call the **[[The Yeast Pathway Kit\|Yeast Pathway Kit]]** (YPK). See our [publication](https://pubmed.ncbi.nlm.nih.gov/26916955) in *ACS Synthetic Biology* for more details.

We use this protocol for rapid construction and expression of large metabolic pathways in baker's yeast _[Saccharomyces cerevisiae](https://en.wikipedia.org/wiki/Saccharomyces_cerevisiae)_ such as the pTA1_FASIIb metabolic pathway expressing twelve genes from *E. coli* and *A. thaliana* [link](https://www.sciencedirect.com/science/article/pii/S221403012300007X) heterologous fatty acid synthesis pathway.

Plasmids in the pTAx series are used to propagate these constructs in *E. coli* or *S. cerevisiae*.

In order to replicate in both *E.coli* and *S. cerevisiae*, a plasmid needs at least:

- a selection marker for *E. coli*
- an origin of replication for *E. coli*
- a selection marker for *S. cerevisiae*.
- an origin of replication for *S. cerevisiae*.

### The underlying problem we would like to solve

The first plasmid we used to express large pathways was called pYPKpw and it has the five functional parts indicated in Table#1:

| Table#1, pYPKpw | part                                                      | function                                                                                                                                                   |
| --------------- | --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                 | [ampR](https://en.wikipedia.org/wiki/Beta-lactamase)      | [selection marker](https://en.wikipedia.org/wiki/Selectable_marker) for *E. coli*.                                                                         |
|                 | [pUC](https://en.wikipedia.org/wiki/PUC19)                | [origin of replication](https://blog.addgene.org/plasmid-101-origin-of-replication) for *E. coli*.                                                         |
|                 | [2µ](https://blog.addgene.org/plasmids-101-yeast-vectors) | multicopy origin of replication for _S. cerevisiae_ from the natural [2µ plasmid](https://www.sciencedirect.com/science/article/abs/pii/S0147619X13000292) |
|                 | [URA3](https://en.wikipedia.org/wiki/URA3)                | [selection marker](https://en.wikipedia.org/wiki/URA3) for for _S. cerevisiae_.                                                                            |
|                 | Δcrp                                                      | a **partial, inactive** *E. coli* cyclic AMP receptor protein or [CRP](https://en.wikipedia.org/wiki/CAMP_receptor_protein) gene.                          |

The last element in the table,  Δcrp is an *E. coli* gene which is inactive and only provide a recombination site. The pathways that we make are meant for _S. cerevisiae_, but we often need to **transfer the pathway to _E. coli_** so we can obtain larger amounts of higher quality DNA for analysis or transformation.

The pUC origin of replication (ORI) results in a **high copy number** of the vector in *E. coli* which is an advantage for obtaining large amounts of DNA. However, we have observed genetic **instability** in *E. coli* for some large pathways that we suspect is linked to high copy number. Our experience is that a lower copy number provides more stability.
### pTAx vectors for increases stability

We conceived a series of plasmid vectors called pTAx where x is a number from pTA1 .. pTA11 (at the moment). The pTAx vectors were designed to have a relatively **low copy number** in *E. coli* to try to solve the stability problems of pYPKpw.

The pTAx plasmids should have a lower copy number in *E. coli* than pYPKpw since they have the intact **pBR** [[ori\|origin of replication]] (from plasmid pBR322) that includes the [ROP](https://en.wikipedia.org/wiki/Rop_protein) gene, while the pYPKpw has the high-copy pUC origin of replication from the pUC19 plasmid.

pTA1 was the first pTAx plasmid constructed by a former post-doc in the group, **T**atiana **A**ndrevna Pozdniakova, hence the name.

The pTAx vectors are made from **five** genetic elements using in-vivo homologous recombination between five PCR products (Table #2 ➀ .. ➄).

See [[pTAx assembly strategy]] for details of how the five PCR products are assembled into a plasmid..

Each element is a distinct segment from a particular source plasmid. The pTAx vectors are similar to each other, but differ in the selection markers (**yeast marker**) and yeast origin of replication (**yeast ORI**).

| Table#2 | Name     | _E. coli_ marker | _E. coli_ ORI | yeast ORI | yeast marker | MCS  | Constructed by:           | Enzyme to linearize       | 🥶 freezer list number(s) | Sequenced? | Date       |
| ------- | -------- | ---------------- | ------------- | --------- | ------------ | ---- | ------------------------- | ------------------------- | ------------------------- | ---------- | ---------- |
|         |          | ➀                | ➁             | ➂         | ➃            | ➄    |                           |                           |                           |            |            |
|         | pTA1     | ampR             | pBR           | 2µ        | LEU2         | Δcrp | Tatiana Pozdniakova       | AatII, ZraI, FspAI        | µ828, µ928, µ929          | ✅          | 2019-10-xx |
|         | pTA2     | -"-              | -"-           | CEN/ARS   | LEU2         | -"-  | EGB2023                   | AatII, ZraI, FspAI        | µ1814, µ1815, µ1817       |            | 2023-06-01 |
|         | pTA3     | -"-              | -"-           | 2µ        | HIS3         | -"-  | Tatiana Pozdniakova       | AatII, ZraI, FspAI, EcoRV | µ1271                     |            | 2021-07-09 |
|         | pTA4     | -"-              | -"-           | CEN/ARS   | HIS3         | -"-  | EGB2023                   | AatII, ZraI, FspAI, EcoRV | µ1816, µ1818, µ1819       |            | 2023-06-01 |
|         | pTA5     | -"-              | -"-           | 2µ        | KanMX4       | -"-  | Paulo Silva, Julio Freire | AatII, ZraI, FspAI, EcoRV | µ1652                     | ✅          |            |
|         | pTA6     | -"-              | -"-           | CEN/ARS   | KanMX4       | -"-  | GMB20                     | AatII, ZraI, FspAI, EcoRV | µ520                      |            | 2020-12-23 |
| 🔥      | **pTA7** | -"-              | -"-           | 2µ        | TRP1         | -"-  | EGB2025                   | AatII, ZraI, FspAI        | ❓                         | ❓          | ❓          |
|         | pTA8     | -"-              | -"-           | CEN/ARS   | TRP1         | -"-  | GMB20                     | AatII, ZraI, FspAI        | µ521, µ522                |            | 2020-12-23 |
|         | pTA9     | -"-              | -"-           | 2µ        | URA3         | -"-  | Tatiana Pozdniakova       | AatII, ZraI, FspAI        | µ1272                     |            | 2021-07-09 |
|         | pTA10    | -"-              | -"-           | CEN/ARS   | URA3         | -"-  | GMB20                     | AatII, ZraI, FspAI        | µ523                      |            | 2020-12-23 |
|         | pTA11    | -"-              | -"-           | 2µ        | LEU2d        | -"-  | EGB2024                   | AatII, ZraI, FspAI        | µ542                      | ✅          | 2024-05-23 |

This lab course is divided into nine practical classes, see below. Each student attends three of the nine classes. In each practical class, we advance the project towards the finished plasmid.

| link      |       |       |       | Content                                                                                |
| --------- | ----- | ----- | ----- | -------------------------------------------------------------------------------------- |
| [[pTAx/LAB1]]  | PL1   |       |       | Prepare plasmid DNA from E. coli by small scale alkaline lysis (miniprep).             |
| [[pTAx/LAB2]]  |       | PL2   |       | Analyze plasmid DNA by agarose gel.<br>Prepare PCR reactions for each plasmid element. |
| [[pTAx/LAB3]]  |       |       | PL3   | Analyze PCR products by agarose gel.<br>Inoculate *S. cerevisiae* for transformation.  |
| [[pTAx/LAB4]]  | PL1   |       |       | Yeast (*S. cerevisiae*) transformation.                                                |
| [[pTAx/LAB5]]  |       | PL2   |       | *In-silico* assembly of plasmid 💻                                                     |
| [[pTAx/LAB6]]  |       |       | PL3   | Yeast colony PCR                                                                       |
| [[pTAx/LAB7]]  | PL1   |       |       | Analyze colony PCR products by agarose gel<br>Prepare solid LB medium for LAB8         |
| [[pTAx/LAB9]]  |       | PL2   |       | Yeast DNA preparation<br>*E. coli* transformation (Plasmid rescue)                     |
| [[pTAx/LAB9]]  |       |       | PL3   | Plasmid alkaline lysis miniprep with commercial kit.                                   |
| [[pTAx/LAB10]] | (Opt) | (Opt) | (Opt) | Analytical restriction digestion of plasmid DNA.                                       |
