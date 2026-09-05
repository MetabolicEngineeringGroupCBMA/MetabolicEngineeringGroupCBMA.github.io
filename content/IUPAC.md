---
publish: true
---

The IUPAC Extended Genetic Alphabet is a universal nomenclature system that uses single-letter codes to represent degenerate or ambiguous nucleotide bases in DNA and RNA sequences. It expands the standard 4-letter DNA alphabet (A, C, G, T) into a 15-letter alphabet to account for every possible combination of matching nucleotides. This system is used in for designing degenerate PCR primers, defining transcription factor binding motifs, and mapping single nucleotide polymorphisms (SNPs).
## Standard and Ambiguous IUPAC DNA Codes

| IUPAC Code | Represented Base(s) | Base Name / Meaning | Mnemonic / Category |
|---|---|---|---|
| A | A | Adenine | Standard base |
| C | C | Cytosine | Standard base |
| G | G | Guanine | Standard base |
| T | T | Thymine | Standard base |
| R | A or G | Rupine | Purines |
| Y | C or T | PYrimidine | Pyrimidines |
| S | G or C | Strong interaction | 3 Hydrogen bonds |
| W | A or T | Weak interaction | 2 Hydrogen bonds |
| K | G or T | Keto | Bases with a keto group |
| M | A or C | AMino | Bases with an amino group |
| B | C or G or T | Not A | Follows A alphabetically |
| D | A or G or T | Not C | Follows C alphabetically |
| H | A or C or T | Not G | Follows G alphabetically |
| V | A or C or G | Not T / Not U | Follows U alphabetically |
| N | A or C or G or T | aNy base | Completely unknown |

## Complementary Base Pairing for Degenerate Codes
When determining the reverse complement of an ambiguous sequence, each degenerate symbol pairs with a unique counterpart based on its underlying components: [6] 

- R pairs with Y (and vice versa)
- S pairs with S
- W pairs with W
- K pairs with M (and vice versa)
- B pairs with V
- D pairs with H
- N pairs with N

## Modified Bases (Biopython Extension)
In specific bioinformatics environments like [Biopython's IUPAC module](https://biopython.org/docs/1.76/api/Bio.Alphabet.IUPAC.html#Bio.Alphabet.IUPAC.ExtendedIUPACDNA), the concept of an "Extended IUPAC DNA" alphabet is sometimes utilized to include specialized or modified nucleosides alongside standard ambiguity mappings. For example, the character B is repurposed to denote 5-bromouridine rather than its traditional "not A" meaning.

The IUPAC amino acid codes are:

```
A ALA alanine                         P PRO proline
B ASX aspartate or asparagine         Q GLN glutamine
C CYS cystine                         R ARG arginine
D ASP aspartate                       S SER serine
E GLU glutamate                       T THR threonine
F PHE phenylalanine                   U     selenocysteine
G GLY glycine                         V VAL valine
H HIS histidine                       W TRP tryptophan
I ILE isoleucine                      Y TYR tyrosine
K LYS lysine                          Z GLX glutamate or glutamine
L LEU leucine                         X     any
M MET methionine                      *     translation stop
N ASN asparagine                      -     gap of indeterminate length
```
