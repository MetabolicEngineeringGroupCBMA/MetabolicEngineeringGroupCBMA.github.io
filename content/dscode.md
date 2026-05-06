This document defines `dscode`, an extension or a super set to the IUPAC DNA alphabet (IUPAC). This extension and allows unambiguous description of a double stranded DNA molecule with single stranded regions (such as "sticky" ends) using a single sequence of characters. This makes it directly applicable for sequence classes holding sequences as a string, such as the BioPython Seq objects. The `dscode` alphabet has been implemented in the Dseq class in pydna, a subclass of the Biopython Seq class.

## IUPAC

The IUPAC DNA alphabet is a set of symbols designated by the International Union of Pure and Applied Chemistry (IUPAC)
to represent nucleotide bases in DNA sequences, including ambiguity codes for cases where multiple nucleotides are possible
at a particular position. The symbols and their meanings are listed below:

1. **A** - Adenine
2. **T** - Thymine
3. **C** - Cytosine
4. **G** - Guanine

**Ambiguity codes** (representing multiple possible nucleotides):

1. **R** - Purine (A or G)
2. **Y** - Pyrimidine (C or T)
3. **S** - Strong interaction (G or C)
4. **W** - Weak interaction (A or T)
5. **K** - Keto group (T or G)
6. **M** - Amino group (A or C)
7. **B** - Not A (C, G, or T)
8. **D** - Not C (A, G, or T)
9. **H** - Not G (A, C, or T)
10. **V** - Not T (A, C, or G)
11. **N** - Any nucleotide (A, T, C, or G)

These symbols allow representing DNA sequences, when there is uncertainty in base composition at specific positions.
However, they do not address the single or double strandedness of DNA.

## dscode

The dscode alphabet is a super set of the IUPAC alphabet. The symbols take on a different meaning as each symbol represent a base pair  (a base in a DNA strand and its complementary base on the other strand) instead of a single base.

| Alphabet   | Symbol | Complement | Bases                                       | dscode meaning |
| ---------- | ------ | ---------- | ------------------------------------------- | -------------- |
| IUPAC      | G      | C          | G                                           | G/C            |
| "          | A      | T          | A                                           | A/T            |
| "          | T      | A          | T                                           | T/A            |
| "          | C      | G          | C                                           | C/G            |
| "          | R      | Y          | G or A                                      | R/Y            |
| "          | Y      | R          | T or C                                      | Y/R            |
| "          | M      | K          | A or C                                      | M/K            |
| "          | K      | M          | G or T                                      | K/M            |
| "          | S      | S          | G or C                                      | S/S            |
| "          | W      | W          | A or T                                      | W/W            |
| "          | H      | D          | A or C or T                                 | H/D            |
| "          | B      | V          | G or T or C                                 | B/V            |
| "          | V      | B          | G or C or A                                 | V/B            |
| "          | D      | H          | G or A or T                                 | D/H            |
| "          | N      | N          | G or A or T or C                            | N/N            |
| **dscode** | U      | O          | U in top strand, A in complementary strand  | U/A            |
| "          | O      | U          | A in top strand, U in complementary strand  | A/U            |
| "          | E      | F          | A in top strand, complementary strand empty | A/◻            |
| **"**      | I      | J          | C "                                         | C/◻            |
| **"**      | P      | Q          | G "                                         | G/◻            |
| **"**      | X      | Z          | T "                                         | T/◻            |
| **"**      | Z      | X          | A in complementary strand, top strand empty | ◻/A            |
| **"**      | Q      | P          | C "                                         | ◻/C            |
| **"**      | J      | I          | G "                                         | ◻/G            |
| **"**      | F      | E          | T "                                         | ◻/T            |
| "          | !      | A          | A in upper strand A in lower strand         | A/A            |
| "          | #      | C          | A in upper strand C in lower strand         | A/C            |
| **"**      | \$      | G          | A in upper strand G in lower strand         | A/G            |
| **"**      | %      | A          | C in upper strand A in lower strand         | C/A            |
| **"**      | &      | C          | C in upper strand C in lower strand         | C/C            |
| "          | \*      | T          | C in upper strand T in lower strand         | C/T            |
| "          | (      | A          | G in upper strand A in lower strand         | G/A            |
| **"**      | )      | G          | G in upper strand G in lower strand         | G/G            |
| **"**      | <      | T          | G in upper strand T in lower strand         | G/T            |
| **"**      | >      | C          | T in upper strand C in lower strand         | T/C            |
| **"**      | @      | G          | T in upper strand G in lower strand         | T/G            |
| **"**      | :      | T          | T in upper strand T in lower strand         | T/T            |
| **"**      | ?      | G          | U in upper strand G in lower strand         | U/G            |
| **"**      | \[      | C          | U in upper strand C in lower strand         | U/C            |
| **"**      | ]      | T          | U in upper strand T in lower strand         | U/T            |

The symbols PEXI and QFZJ that are not occupied by the extended IUPAC alphabet were adopted to imply single stranded DNA on either
strand where no complementary bas exist.

```
GATCaUaAa                   ad-hoc representation
    tAtUtCTAG


PEXIaUaOaQFZJ               representation using dscode
```

The choice of symbols for the dscode extension facilitate intuitive recognition of compatible single stranded regions, i.e. sticky-ends. The symbols that can anneal are adjacent in the alphabet eg. `Q-P`, `E-F`, `I-J`, only broken by X-Z due to necessity as Y is a parth of the IUPAC alphabet.

```
            ...QFZJ    PEXI...

			...  		 GATC...
		    ...CATG   	 ...
```

## Example

DNA molecules with compatible terminal 3'- single strand overhangs:

```
QFZJaaaPEXI    QFZJaaaPEXI           representation using dscode

	aaaGATC        aaaGATC           ad-hoc representation
CTAGttt        CTAG
```

## alphabets

```
ASCII CAPS  = ABCDEFGHIJKLMNOPQRSTUVWXYZ
IUPAC       = ABCD  GH  K MN   RST VW Y
dscode      =     EF  IJ L  OPQ   U  X Z   +  IUPAC

punctuation = ! # $ % & * + ( ) < = > @ /: ' , - . ; ? [ \ ] ^ _ ` { | } ~ "
```

## Different representations of double stranded DNA:

```
>format1 alphabet=dscode
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
