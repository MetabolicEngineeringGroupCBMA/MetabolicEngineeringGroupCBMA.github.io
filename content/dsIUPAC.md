This document defines an extension to the IUPAC DNA alphabet (IUPAC) tailored for double stranded DNA.
This extension is called dsIUPAC and allows unambiguous description of a double stranded DNA molecule
with single stranded regions (such as "sticky" ends) using a single sequence of characters.

## IUPAC

The IUPAC DNA alphabet is a set of symbols designated by the International Union of Pure and Applied Chemistry (IUPAC)
to represent nucleotide bases in DNA sequences, including ambiguity codes for cases where multiple nucleotides are possible
at a particular position. The symbols and their meanings are listed below:

1. **A** - Adenine
2. **T** - Thymine
3. **C** - Cytosine
4. **G** - Guanine

**Ambiguity codes** (representing multiple possible nucleotides):

5. **R** - Purine (A or G)
6. **Y** - Pyrimidine (C or T)
7. **S** - Strong interaction (G or C)
8. **W** - Weak interaction (A or T)
9. **K** - Keto group (T or G)
10. **M** - Amino group (A or C)
11. **B** - Not A (C, G, or T)
12. **D** - Not C (A, G, or T)
13. **H** - Not G (A, C, or T)
14. **V** - Not T (A, C, or G)
15. **N** - Any nucleotide (A, T, C, or G)

These symbols allow for flexibility in representing DNA sequences, especially when there is uncertainty in base composition
at specific positions. However, they do not address the single or double strandedness of DNA.

## dsIUPAC

The dsIUPAC alphabet is a superset of the IUPAC alphabet. The symbols take on a differen meaning in that each symbol represent a basepair
(a base in a DNA strand and its complementary base on the other strand. The alphabet uses an additional ten symbols to represen
single stranded regions where there is no complementary base. See table below. The dsIUPAC remains 100% comatible with the IUPAC alphabet.

[link](https://docs.google.com/spreadsheets/d/1dRCMjoGKQnyQeNq6aKs1utTZXfI7yLECPGmVwJpCSEo/edit?usp=sharing)

| Alphabet    | Symbol | Complement | Bases                                       | dsIUPAC extended meaning |
| ----------- | ------ | ---------- | ------------------------------------------- | ------------------------ |
| IUPAC       | G      | C          | G                                           | G/C                      |
| "           | A      | T          | A                                           | A/T                      |
| "           | T      | A          | T                                           | T/A                      |
| "           | C      | G          | C                                           | C/G                      |
| "           | R      | Y          | G or A                                      | R/Y                      |
| "           | Y      | R          | T or C                                      | Y/R                      |
| "           | M      | K          | A or C                                      | M/K                      |
| "           | K      | M          | G or T                                      | K/M                      |
| "           | S      | S          | G or C                                      | S/S                      |
| "           | W      | W          | A or T                                      | W/W                      |
| "           | H      | D          | A or C or T                                 | H/D                      |
| "           | B      | V          | G or T or C                                 | B/V                      |
| "           | V      | B          | G or C or A                                 | V/B                      |
| "           | D      | H          | G or A or T                                 | D/H                      |
| "           | N      | N          | G or A or T or C                            | N/N                      |
| **dsIUPAC** | U      | O          | U in top strand, A in complementary strand  | U/A                      |
| "           | O      | U          | A in top strand, U in complementary strand  | A/U                      |
| "           | E      | F          | A in top strand, complementary strand empty | A/◻                      |
| **"**       | I      | J          | C "                                         | C/◻                      |
| **"**       | P      | Q          | G "                                         | G/◻                      |
| **"**       | X      | Z          | T "                                         | T/◻                      |
| **"**       | Z      | X          | A in complementary strand, top strand empty | ◻/A                      |
| **"**       | Q      | P          | C "                                         | ◻/C                      |
| **"**       | J      | I          | G "                                         | ◻/G                      |
| **"**       | F      | E          | T "                                         | ◻/T                      |
| "           | !      | A          | A in upper strand A in lower strand         | A/A                      |
| "           | #      | C          | A in upper strand C in lower strand         | A/C                      |
| **"**       | $      | G          | A in upper strand G in lower strand         | A/G                      |
| **"**       | %      | A          | C in upper strand A in lower strand         | C/A                      |
| **"**       | &      | C          | C in upper strand C in lower strand         | C/C                      |
| "           | *      | T          | C in upper strand T in lower strand         | C/T                      |
| "           | (      | A          | G in upper strand A in lower strand         | G/A                      |
| **"**       | )      | G          | G in upper strand G in lower strand         | G/G                      |
| **"**       | <      | T          | G in upper strand T in lower strand         | G/T                      |
| **"**       | >      | C          | T in upper strand C in lower strand         | T/C                      |
| **"**       | @      | G          | T in upper strand G in lower strand         | T/G                      |
| **"**       | :      | T          | T in upper strand T in lower strand         | T/T                      |
| **"**       | ?      | G          | U in upper strand G in lower strand         | U/G                      |
| **"**       | [      | C          | U in upper strand C in lower strand         | U/C                      |
| **"**       | ]      | T          | U in upper strand T in lower strand         | U/T                      |




The symbols PEXI and QFZJ that are not occupied by the extended IUPAC alphabet were adopted to imply single stranded DNA.

The choice of symbols for the dsIUPAC extension facilitate intuitive recognition of compatible single stranded regions, i.e. sticky-ends.

## Example

Two double stranded DNA molecules with compatible terminal 5'- single strand overhangs:

```
GATCaUaAa                   ad-hoc representation
    tAtUtCTAG


PEXIaUaOaQFZJ               representation using dsIUPAC
```

We can easily recognize that alphabetically,  `P` is followed by `Q`, `E` by `F` and `I` by `J`.
This symmetry is only broken by the `X`, `Z` pair of necessity since `Y` is already used in the IUPAC alphabet.

DNA molecules with compatible terminal 3'- single strand overhangs:

```
QFZJaaaPEXI    QFZJaaaPEXI           representation using dsIUPAC

	aaaGATC        aaaGATC           ad-hoc representation
CTAGttt        CTAG
```

## alphabets
```
ASCII CAPS  = ABCDEFGHIJKLMNOPQRSTUVWXYZ
IUPAC       = ABCD  GH  K MN   RST VW Y
dsIUPAC     =     EF  IJ L  OPQ   U  X Z   +  IUPAC

punctuation = ! # $ % & * + ( ) < = > @ /: ' , - . ; ? [ \ ] ^ _ ` { | } ~ "
```


## Different representations of double stranded DNA:

```

>format1 alphabet=dsIUPAC
PEXIGULAOCQFZJ

>format2 two strings & space
GATCGUAAAC
    CAUTUGCTAG

>format3 two strings & hyphen
GATCGUAAAC----
----CAUTUGCTAG

>format4 two strings & pipe
GATCGUAAAC||||
||||CAUTUGCTAG

>format5 three strings, pipe & hyphen
GATCGUAAAC----
||||||||||||||
----CAUTUGCTAG
```
