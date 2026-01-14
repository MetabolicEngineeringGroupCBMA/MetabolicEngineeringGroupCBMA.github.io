### Description

Notes from the "*Cloning documentation workshop*" held on 11th of April 2025. Of the twelve participants, two were PhD students, two third-year students and eight second-year students of the Bachelor in Applied Biology and in Chemical and Biological Engineering of the University of Minho. Instructors were [Manuel Ramirez](https://github.com/manulera) attending remotely and [Björn Johansson](https://github.com/BjornFJohansson) attending in person.

![[Open Cloning FAIRification exercise_001.png.jpg|318x98]]

![[Open Cloning FAIRification exercise_002.png.jpg|320x116]]

### Objective

The objective of the exercise was to analyse a number of selected journal articles to assess the reproducibility of genetic constructs described in the article. The articles were collected from references for plasmids submitted to the [addgene](https://www.addgene.org/) plasmid repository. Articles are listed in the table below and in [this](https://docs.google.com/spreadsheets/d/1UuljFV8-FEAFT3jnHevuTmERE0VNCNRSH693Y2Uq7Ag/edit?usp=sharing) google sheet.

| PMID          | Title                                                                                                                                                                                                       | Journal                                                | Assigned to    |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | -------------- |
| PMID:35293864 | Microtubule rescue at midzone edges promotes overlap stability and prevents spindle collapse during anaphase B.                                                                                             | eLife                                                  | Henrique       |
| PMID:11526030 | Xylulokinase overexpression in two strains of Saccharomyces cerevisiae also expressing xylose reductase and xylitol dehydrogenase and its effect on fermentation of xylose and lignocellulosic hydrolysate. | Applied and environmental microbiology                 | Maria Inês     |
| PMID:16597698 | GUP1 of Saccharomyces cerevisiae encodes an O-acyltransferase involved in remodeling of the GPI anchor.                                                                                                     | Molecular biology of the cell                          | Gonçalo Amaro  |
| PMID:7737504  | Yeast vectors for the controlled expression of heterologous proteins in different genetic backgrounds.                                                                                                      | Gene                                                   | Faezeh Ghasemi |
| PMID:16322578 | Gateway vectors for the production of combinatorially-tagged His6-MBP fusion proteins in the cytoplasm and periplasm of Escherichia coli.                                                                   | Protein science : a publication of the Protein Society |                |
| PMID:39007160 | Versatile Cloning Strategy for Efficient Multigene Editing in Arabidopsis.                                                                                                                                  | Bio-protocol                                           | Inês           |
| PMID:17033696 | Generation of gene deletions and gene replacements in Escherichia coli O157:H7 using a temperature sensitive allelic exchange system.                                                                       | Biological procedures online                           | Rodolfo        |
| PMID:20569222 | Overlap extension PCR cloning: a simple and reliable way to create recombinant plasmids.                                                                                                                    | BioTechniques                                          | Pedro ; Maria  |
| PMID:12185276 | Cloning of complete genome sets of six dsRNA viruses using an improved cloning method for large dsRNA genes.                                                                                                | The Journal of general virology                        | Manu           |
| PMID:25774528 | Optimal cloning of PCR fragments by homologous recombination in Escherichia coli.                                                                                                                           | PloS one                                               | Patrícia       |
| PMID:26348330 | Cloning Should Be Simple: Escherichia coli DH5α-Mediated Assembly of Multiple DNA Fragments with Short End Homologies.                                                                                      | PloS one                                               | Miguel         |
| PMID:27264908 | IVA cloning: A single-tube universal cloning system exploiting bacterial In Vivo Assembly.                                                                                                                  | Scientific reports                                     | Beatriz        |
| PMID:28837659 | In vivo cloning of up to 16 kb plasmids in E. coli is as simple as PCR.                                                                                                                                     | PloS one                                               | João           |
| PMID:12202778 | Cre recombinase-mediated inversion using lox66 and lox71: method to introduce conditional point mutations into the CREB-binding protein.                                                                    | Nucleic acids research                                 |                |
| PMID:12491882 | Maltose-binding protein as a solubility enhancer.                                                                                                                                                           | Methods in molecular biology (Clifton, N.J.)           |                |
| PMID:17272834 | A generic method for the production of recombinant proteins in Escherichia coli using a dual hexahistidine-maltose-binding protein affinity tag.                                                            | Methods in molecular biology (Clifton, N.J.)           |                |

### Tools

![[Cloning documentation workshop_004.png|344x214]]

[OpenCloning](https://opencloning.org) is an Open-Source web application to plan and document cloning. It permits the user to build cloning
strategies using a graphical point and click interface. The end result is a graphical representation of the cloning strategy as well as
as strategy formally expressed in JSON.

![[Cloning documentation workshop_005.png|395x237]]

[Pydnaweb](https://pydnaweb.streamlit.app/) offers web interfaces for selected functionality from the [pydna](https://github.com/pydna-group/pydna) Python package. Pydnaweb offers PCR simulation
and restriction simulation among other helpful techniques.

![[Cloning documentation workshop_006.png|295x197]]

[pLannotate](http://plannotate.barricklab.org) re-annotates plasmids and indicate functional sub units.
### Method

The most productive workflow consisted of identifying genetic constructs (mostly plasmids) mentioned prominently in the beginning of the results section of the publication. Subsequently, the materials section was scanned for descriptions of the plasmid construction strategy. Potential supplementary data was also scanned for primer and vectors sequences.

The students filled in a Github issue template (a google doc version [here](https://docs.google.com/document/d/1UqExPvMSS4n3aRx2gxNs2EZGUYXgzVtKbGp2uvQ4pFg/edit?usp=drive_link)) detailing their findings together with a JSON file produced by OpenCloning.

Here is a link to [detailed](https://github.com/OpenCloning/cloning_workshop) instructions for the workshop.

---

Example of a note exchanged during the session:

Info for student H: The cloning information is in the supplementary file (you can download this from the publication page), It's in the "Figures and Data" tab. From there, you can download an excel file and Plasmid map of pFa6a-mCherry-ase1-kanMX6. With that, you can reproduce the construction of the allele mCherry-ase1:kanMX6. You would have to find the sequence of the gene ase1 in the genome of Schizosaccharomyces pombe, do the PCR with the indicated primers, and simulate a homologous recombination.

---

Email inviting students to the workshop:

Hi all,

The *Cloning Documentation Workshop* will happen tomorrow at 15:00 and last for a maximum of two hours. The exercise will be held in the Dept of Biology library (Ed6 1.94) just next to my office.

1. Please bring your computer
2. Please sign up for a free **GitHub** account [here](https://github.com/). This is needed to fill in some forms at the end of the exercise.
2. Bookmark this [link](https://etherpad.wikimedia.org/p/OpenCloningExercise). It goes to an online shared text editor where we can share information.

The participants will be given a scientific **journal article** that depends on a genetic construct (such as a plasmid).

The goal is to:

1. Assess if the article contains enough information to recreate the genetic construct.
2. Recreate this using [OpenCloning](https://opencloning.org/). This is a graphic tool that simulates cloning experiments.
3. Upload the resulting cloning strategy to Github.

This is meant to be an assessment of the published articles, rather than the students. This means that we will help you as 
much as we can. 

See you all tomorrow!
/bjorn
