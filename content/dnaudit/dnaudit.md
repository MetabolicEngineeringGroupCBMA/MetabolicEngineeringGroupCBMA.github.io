---
publish: true
---

This document describes the _dnaudit_ standard for documentation of genetic constructs in a light plain text format and a a combination of yaml, markdown and Genbank files.

The goal of this standard is to facilitate documentation that is clear and unambiguous, yet with minimal markup.

The documentation generated using this standard shows step-by step how a genetic construct was made so that it can be reproduced
while at the same time making it easier to _preserve_ and _share_ genetic material.

A genetic construct can be for example:

- a plasmid made from parts of other plasmids or chromosomal DNA fragments
- DNA integrated in the genome of an organism by CRISPr

The documentation for a genetic construct consists of a a collection of text files in a folder 📁 with optional sub folders.
Each text file contains a description of one molecular biology [unit-operations](https://en.wikipedia.org/wiki/Unit_operation) consisting of sequences in FASTA format.

A very reduced, easy to remember collection of key words describe each unit operation. Examples of unit operation are for
example PCR or homologous recombination.

A unit operation is delineated by a header (Table #1) and the next header or the end of the text file.

A unit operation contains a series of input sequences in a specified order as well as at least one resulting sequence.
The file can (and should) also contain comments explaining the aim of the experiment.

| Table#1 | Header         | Unit operation                                             |
| ------- | -------------- | ---------------------------------------------------------- |
|         | `# pcr`        | PCR reaction                                               |
|         | `# cut`        | Restriction digestion with one or more restriction enzymes |
|         | `# crispr`     | CRISPr digestion                                           |
|         | `# ligation`   | Ligation with a DNA ligase                                 |
|         | `# assembly`   | Homologous recombination                                   |
|         | `# fusion_pcr` | fusion PCR                                                 |
|         | `# gateway`    | gateway cloning                                            |
|         | `# objective`  | The end goal                                               |

🔑 Additionally, there are some reserved key/value expressions (Table#2) with special meaning.

🚨Key/Value Pairs should contain no white space characters.

| Table#2 | Reserved Key/Value Pairs   | Meaning                                | Note                                                                                              |     |
| ------- | -------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------- | --- |
|         | `cdseguid=...`             | Checksum for a circular dsDNA sequence | Implies a circular molecule even in the absence of `topology=...`                                 |     |
|         | `ldseguid=...`             | Checksum for a linear dsDNA sequence   | Implies a linear molecule even in the absence of `topology=...`                                   |     |
|         | `csseguid=...`             | Checksum for a circular ssDNA sequence | Implies a circular molecule even in the absence of `topology=...`                                 |     |
|         | `lsseguid=...`             | Checksum for a linear ssDNA sequence   | Implies a linear molecule even in the absence of `topology=...`                                   |     |
|         | `alphabet=dsIUPAC`         | Symbols are [[dscode]].               | This is the default DNA symbol table. This is a super set of the extended [[IUPAC]] nomenclature. |     |
|         | `topology=circular/linear` | Molecule is either circular or linear  |                                                                                                   |     |
|         | `molecule=protein/DNA/RNA` | Indicating a protein sequence.         |                                                                                                   |     |

These reserved Key/Value should be placed after the identifier in the FASTA header.

## Constraints

1. All relevant files have to be in the same project folder tree.
2. Unit-operation snippets must have an `.md` file extension.
3. A unit-operation starts with one of the reserved words from Table#1 or optionally yaml front matter.
4. Sequences in the unit-operation files must be in FASTA [[Genbank|format]].
5. File names must be unique in the project folder tree.
6. Sequences are identified by their name (This is _not_ necessarily the same as the file name of a sequence file).
7. There can be only one identifier for a certain DNA sequence in the project folder.

The [PydnaWeb](https://pydna.pythonanywhere.com) simulation tools can be helpful when preparing unit-operation snippets.

## Examples:

[[dnaudit/pcr]]
[[dnaudit/cut]]
[[dnaudit/crispr]]
[[dnaudit/ligation]]
[[dnaudit/assembly]]
[[dnaudit/fusion_pcr]]
[[dnaudit/gateway]]
[[dnaudit/objective]]

## More examples

A lactose metabolic [pathway](https://github.com/MetabolicEngineeringGroupCBMA/Lactose-Pathway) for _S. cerevisiae_ was formulated using this method. The pathway contains two expression cassettes with the Kluyveromyces lactis beta-D-galactosidase `LAC4` and  the `LAC12` Kluyveromyces lactis LAC12 gene for lactose permease. You can download the files by using the `Code` button and then the `Download ZIP` button:

![[dlzip.png]]

Briefly:

1. LAC4 was pcr amplified from chromosomal DNA.
2. The PCR product was cloned in the pYPKa vector in the _Aj&#x69;_&#x49; site.
3. A DNA fragment was pcr amplified from the pYPKa\_A\_LAC4 vector
4. A promoter was amplified from the pYPKa\_Z\_PDC1 plasmid
5. A terminator was amplified from the pYPKa\_E\_PGI1 plasmid
6. The promoter gene and terminator and the vector pYPKpw digested with _Zr&#x61;_&#x49; was joined by recombination to form the `pYPK0_PDC1_KlLAC4_PGI1` circular plasmid.

The same procedure was performed for the LAC12 but with the `pYPKa_Z_PGI1` vector for the promoter and `pYPKa_E_TPI1` for terminator. The resulting vector is called `pYPK0_PGI1_KlLAC12_TPI1`.

The two expression cassettes were pcr amplified and joined by homologous recombination with a pYPKpw vector digested with _Zr&#x61;_&#x49; resulting in the
`pYPK0_PDC1_KlLAC4_PGI1_KlLAC12_TPI1` vector expressing both genes.

In this example, each file contain only one snippet, but all snippets could be put in one file.

The advantage of separate files is that they can be reused.

Each file name starts with the header of the snippet, like "pcr\_...".
This is optional, but makes it easier to sort the files.
