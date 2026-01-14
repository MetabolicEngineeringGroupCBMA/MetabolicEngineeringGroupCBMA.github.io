## linker


### Linker#1

L1: GGGGSGGGGS

GGAGGTGGAGGTTCTGGTGGAGGTGGTTCA

Ref?? Rosana

### Linker#2

http://parts.igem.org/Protein_domains/Linker

GlyGlyGlyGlyGlySer = GGT GGA GGT GGA GGA TCT

"Several other types of flexible linkers, including KESGSVSSEQLAQFRSLD and EGKSSGSGSESKST"

```
Chen, Xiaoying, Jennica L. Zaro, and Wei-Chiang Shen. 2013. “Fusion Protein
Linkers: Property, Design and Functionality.” Advanced Drug Delivery Reviews
65 (10) (October): 1357–1369.
```


EGKSSGSGSESKST    14 aa = 14 * 3 = 42 bp   <====<<<<   Good size
ESGSVSSEQLAQFRSLD 18 aa = 18 * 3 = 54 bp


The two linkers above are from:
```
Bird, R. E., K. D. Hardman, J. W. Jacobson, S. Johnson, B. M. Kaufman, S. M.
Lee, T. Lee, S. H. Pope, G. S. Riordan, and M. Whitlow. 1988. “Single-Chain
Antigen-Binding Proteins.” Science 242 (4877) (October 21): 423–426.
```

DNA sequence made:
https://www.bioinformatics.org/sms2/rev_trans.html
https://www.kazusa.or.jp/codon/cgi-bin/showcodon.cgi?species=4932&aa=1&style=GCG

gaaggtaaatcttctggttctggttctgaatctaaatctac
E  G  K  S  S  G  S  G  S  E  S  K  S  T


---

Optimized linker for yEGFP fusion proteins:

GDGAGL (Gly-Asp-Gly-Ala-Gly-Leu)

DNA: `ggtgacggtgctggttta`

```
Sheff, M. A., & Thorn, K. S. (2004). Optimized cassettes for fluorescen
protein tagging in Saccharomyces cerevisiae. Yeast , 21(8), 661–670.
```

---

Other GFP linker:

GSAGSAAGSGEF (as good as the (GGGGS)4 linker, but less likely for the coding DNA sequence to be removed by homologous recombination)

DNA: `GGATCCGCTGGCTCCGCTGCTGGTTCTGGCGAATTC`

[https://www.nature.com/articles/nbt0799_691](https://www.nature.com/articles/nbt0799_691)

---

Other info:


More information about fusion protein linkers:
[https://www.ncbi.nlm.nih.gov/pubmed/23026637](https://www.ncbi.nlm.nih.gov/pubmed/23026637)


https://www.researchgate.net/post/What_is_the_best_linker_for_a_fusion_protein

There are linkers based on the same principle than the (GGGGS)n which I find
superior as they don't have repeats that can lead to homologous recombination.
One example: GSAGSAAGSGEF. ref for the GSAGSAAGSGEF linker:

Waldo, G.S., Standish, B.M., Berendzen, J., and Terwilliger, T.C. (1999). Rapid
protein- folding assay using green fluorescent protein. Nat. Biotechnol. 17,
691–695.

ref for other similar linkers:

Chen, X., Zaro, J.L., and Shen, W.-C. (2013). Fusion protein linkers: property,
design and functionality. Adv. Drug Deliv. Rev. 65, 1357–1369.
