---
publish: true
---

# FAIR principles

Imagine that you have a dataset and have written a Python script that produces a useful result. Could another student or researcher find the data, understand them, and use them in a different project? Could another researcher run the Python script on their computer? Could **you** do the same six months from now?

Following FAIR principles helps us plan for this reuse.

The plasmid sequence below was once mailed to me a raw DNA sequence in a MS word file:

![[Mestrado em Biologia Computacional Molecular e Ambiental/FAIR1xnppt.png]]

What is wrong with that?

---

## Why do we need FAIR?

Imagine receiving these files by email:

```text
data_final.xlsx
sequences_new.txt
analysis_final_v3.py
```

The spreadsheet has columns named `sample`, `value`, and `group`. There are no units, no source, and
no explanation of the groups.

The script works on the author's computer, but it expects a file at `C:/Users/Ana/Desktop/data.xlsx`.

Question **What would you need before you could trust and reuse this analysis?**

README!

---

## What does FAIR mean?

The [FAIR Principles](https://www.go-fair.org/fair-principles/) are a set of guidelines published in 2016 to help humans and machines find, access, combine, and reuse digital data. Standing for **Findable, Accessible, Interoperable, and Reusable**, they maximize the value and transparency of research and enterprise data.

### Findable (F)

Data and metadata must be easy to locate for both people and computer systems.

- **Persistent Identifiers:** Assign global, unique identifiers like DOIs.
- **Rich Metadata:** Describe data thoroughly with clear labels.
- **Searchable Indices:** Register or index the data in a public or domain-specific repository.

### Accessible (A)

Once found, users and systems must know how to retrieve the data.

- **Open Protocols:** Use standard, free, and universally implemented communication methods (like HTTP).
- **Authentication:** Support security or authorization procedures if data must be restricted.
- **Persistent Metadata:** Ensure metadata remains available even if the underlying data is deleted.

### Interoperable (I)

Data must integrate and work smoothly with other datasets, apps, or workflows.

- **Shared Languages:** Use formal, **open**, and broadly applicable languages and formats for knowledge representation.
- **Standard Vocabularies:** Apply FAIR-compliant glossaries, ontologies, and community standards.
- **Qualified References:** Include clear links or pointers to related datasets.

### Reusable (R)

Data must have enough context and clarity so it can be reliably used in new projects.

- **Clear Licenses:** Attach explicit usage and licensing terms (e.g., Creative Commons).
- **Detailed Provenance:** Document the origin, history, and processing steps of the data.
- **Community Standards:** Follow strict domain-specific best practices.

[Wilkinson et al. (2016): The FAIR Guiding Principles](https://doi.org/10.1038/sdata.2016.18)

---

## Data, metadata and provenance

- **Data** are the observations or sequences you analyse.
- **Metadata** explain what those data represent.
- **Provenance** records where they came from and how they were produced or changed.

For a DNA sequence, useful context includes:

- Organism, strain, and gene.
- Database accession **and version**.
- Whether the sequence is genomic DNA, a CDS, or a protein.
- Retrieval date and source.
- Any trimming, reverse complementation, or other transformation.

---

## Time and date

Use the ISO8604 date format. IT is the only one that makes sense.

![](https://imgs.xkcd.com/comics/iso_8601.png)

Just do it!

---

## F - Findable

- Bottom-up give you files meaningful names. `analysis023.dat` compared to `2026-10-16_analysis_Oct_spectrophotometric_activity_assay_data.dat`
- Give the project a meaningful title.
- Record source accessions and dataset identifiers in your ==README.md==.
- Describe the organism and biological question.
- For a shared release, consider a repository that assigns a [[DOI]].

Compare these descriptions:

```text
Some yeast sequences
```

and

```text
Coding sequences of selected Saccharomyces cerevisiae genes used to compare sequence length and GC content
```

---

## A - Accessible

Identifiers should lead to a standard retrieval method. Authentication may be required; metadata should remain available if the data disappear.

For your project:

- Explain where the input files can be obtained.
- Provide download instructions or a retrieval script.
- State any access restrictions.
- Avoid relying on a file that exists only on your laptop.

**Can someone obtain the input files using only your instructions?**

FAIR is not necessarlyi open data, FAIR does not require unrestricted access.

Sensitive clinical human data may need controlled access while public metadata explain their existence and access conditions.

---

## I - Interoperable

Use shared representations and vocabularies, and explicit relationships between records.

For your project:

- Use established biological formats where appropriate: FASTA or GenBank, for example.
- Use stable sample IDs consistently across files.
- Use database identifiers to connect sequences, organisms, and annotations.
- Document column meanings and units.

```csv
sample_id,organism,temperature_C
S01,Saccharomyces cerevisiae,30
S02,Saccharomyces cerevisiae,37
```

A CSV file is easy to read in Python, but its meaning still needs documentation. Does `temperature_C` mean growth temperature or measurement temperature?

FAIR compliant formats 😊:

- CSV/TSV [info](https://en.wikipedia.org/wiki/Comma-separated_values) /[info](https://en.wikipedia.org/wiki/Tab-separated_values)
- XML [info](https://www.w3schools.com/xml/xml_whatis.asp)
- JSON [info](https://www.json.org/json-en.html)
- yaml [info](https://learnxinyminutes.com/yaml/)
- toml [info](https://toml.io/en/)

Proprietary or closed binary formats ⛔

- MS PowerPoint (.ppt/.pptx), MS Access (.mdb/.accdb)
- Apple Pages, Numbers, Keynote
- Adobe Illustrator (.ai), Photoshop (.psd), InDesign (.indd)
- MATLAB .mat (older, proprietary versions), SAS (.sas7bdat), SPSS (.sav), Stata (.dta)
- Origin (.opj), GraphPad Prism (.pzfx/.prism), SnapGene (.dna), Geneious, Vector NTI, and similar vendor-specific project files
- Vendor-specific instrument raw files (e.g. Thermo .raw, Agilent .d, Waters .raw, Bruker .baf/.tdf, ABI .ab1 as the only copy) without a documented open conversion

Formats that lose information or are hard to parse

- PDF as the sole carrier of tables or data (fine for reports, poor for data reuse)
- Data embedded in images (JPEG, PNG screenshots of tables or gels without underlying data)
- Lossy compression of primary data (JPEG for microscopy or gel images)
- Scanned documents without OCR or structured transcription
- Free-text .doc/.rtf with data tables embedded

Formats that are open but poorly suited

- Unstructured plain-text dumps without a schema or header definition
- CSV with undocumented delimiters, encodings, units, or merged or multi-row headers
- Pickle (.pkl), RData/.rds, and Python/R workspace dumps: language-specific, version-fragile, and a security risk when loading
- Excel-exported CSV with locale-dependent decimal commas, date autoconversion (e.g. gene names like SEPT2 turned into dates)
- SQLite/other DB dumps without exported schema and documentation (acceptable if documented, but not self-describing for most users)

Compressed or container formats without documentation

- Proprietary archives (.rar, .7z are open but less widely supported than .zip or .tar.gz)
- Custom binary formats with no published specification

Better open alternatives for common cases

- Spreadsheets: CSV/TSV (plus a data dictionary), or ODS
- Documents: PDF/A for archiving, plus Markdown, plain text, or ODT for the source
- Tabular/array data: Parquet, HDF5, NetCDF, Zarr
- Sequences/annotations: FASTA, FASTQ, GenBank, GFF3, VCF, SBOL, SBML
- Mass spectrometry: mzML, mzXML, mzTab
- Images: TIFF (uncompressed or lossless), OME-TIFF, PNG for derived figures
- Structured metadata: JSON-LD, YAML, XML with a published schema (e.g. ISA-Tab, RO-Crate)

**Rule of thumb:**

a format is FAIR-friendly if its specification is public, it is readable without licensed software, and it can carry its own metadata or be paired with a documented schema. Where a proprietary format is unavoidable (e.g. instrument raw files), deposit it alongside an open converted version.

---

## R - Reusable

Reuse requires relevant descriptions, an explicit usage licence, provenance, and appropriate community standards.

For your project:

- Explain how the samples and sequences were selected.
- Record **software versions** and **analysis parameters**.
- Describe missing values, exclusions, and limitations.
- Identify the terms that apply to input data and your own outputs.

**Being able to download a file does not tell you what you are allowed to do with it.**

[GO FAIR: the principles and their interpretation](https://www.gofair.foundation/fair-principles)

---

## FAIR and reproducibility

These ideas support each other, but ask different questions.

**Reproducibility:** Can another person run your analysis with the same inputs and obtain the same results?
**Reuse:** Can someone understand and use your data in a new analysis?

A script may run successfully while analyzing poorly documented samples. A well-described dataset may be useful even when the original analysis code is missing.

For this course, aim for **both**: understandable data and an analysis someone else can run.

---

## A biological example: documenting a plasmid

A paper states: “The gene was amplified and cloned into the expression vector.”

What would you need to reconstruct the plasmid?

- Exact template and vector sequences.
- Primer sequences, including added tails.
- The assembly method and relevant parameters.
- The expected final sequence and its annotations.
- Links between the starting materials and the resulting construct.

An image of a plasmid map can help you understand the design. Sequence files and a recorded construction workflow let you investigate it further.

[[Cloning documentation workshop 2025|Our cloning documentation workshop]] used published articles to investigate this problem. OpenCloning can record a construction workflow as a diagram and structured JSON.

---

<!--
## Exercise: audit a published example

Work in pairs. Choose one paper from the table in [[Cloning documentation workshop 2025]]. Open the paper and its supplementary material.

Choose **one construct** and spend 15 minutes collecting evidence.

| Principle | What to investigate | Evidence or missing information |
| --- | --- | --- |
| Findable | Can you locate the sequences and their identifiers? | |
| Accessible | Can you retrieve the files? Are restrictions explained? | |
| Interoperable | Are sequences supplied in usable formats with clear identifiers? | |
| Reusable | Are primers, construction steps, provenance, and usage terms documented? | |

Record URLs, accessions, file names, or specific sections. If you cannot find something, write **“not found in the material examined”**.

Finish with two sentences: **What could you reconstruct? What information would you request from the authors?**

This is an assessment of the documentation, not of your cloning skills.
-->

---

## A README someone else can use

Copy and adapt this outline:

```markdown
# Project title

## Biological question
What am I investigating?

## Input data
Source, accession versions or dataset DOI, retrieval date,
selection criteria, and access or reuse conditions.

## Data description
File formats, identifiers, columns, units, and missing values.

## Run the analysis
Python version, dependencies, and the command to run.

## Results
Output files and how to interpret them.

## Limitations
Assumptions, exclusions, and what the analysis cannot establish.

## Authors and licensing
Who did the work, and which terms apply to code and data?
```

---

## Reading and examples

- [Wilkinson et al. (2016). The FAIR Guiding Principles for scientific data management and stewardship.](https://doi.org/10.1038/sdata.2016.18) The original paper.
- [GO FAIR principles](https://www.gofair.foundation/fair-principles). The individual principles and interpretations.
- [[Cloning documentation workshop 2025]]. Papers and instructions for the audit exercise.
- [D’Ambrosio et al. (2022). A FAIR-compliant parts catalogue for genome engineering and expression control in Saccharomyces cerevisiae.](https://doi.org/10.1016/j.synbio.2022.02.001) An example connecting yeast engineering, data, and analysis notebooks.
