The GenBank [format](https://www.ncbi.nlm.nih.gov/Sitemap/samplerecord.html) (GenBank Flat File Format) consists of an annotation section.
and a sequence section. The start of the annotation section is marked by a
line beginning with the word **"LOCUS"**. The start of sequence section is marked
by a line beginning with the word "**ORIGIN**" and the end of the section is
marked by a line containing **"//"**.

Sequence is expected to be in the standard [[IUPAC]] amino acid or nucleic acid codes.

Filename extensions ".gb" and ".genbank" are common for  text files containing DNA sequences, while ".gp", ".genpept", and ".genpep" are common
for text files containing protein sequences.

A DNA sequence:

```
LOCUS       AF068625                 200 bp    mRNA    linear   ROD 06-DEC-1999
DEFINITION  Mus musculus DNA cytosine-5 methyltransferase 3A (Dnmt3a) mRNA,
			complete cds.
ACCESSION   AF068625 REGION: 1..200
VERSION     AF068625.2  GI:6449467
KEYWORDS    .
SOURCE      Mus musculus (house mouse)
  ORGANISM  Mus musculus
			Eukaryota; Metazoa; Chordata; Craniata; Vertebrata; Euteleostomi;
			Mammalia; Eutheria; Euarchontoglires; Glires; Rodentia;
			Sciurognathi; Muroidea; Muridae; Murinae; Mus.
REFERENCE   1  (bases 1 to 200)
  AUTHORS   Okano,M., Xie,S. and Li,E.
  TITLE     Cloning and characterization of a family of novel mammalian DNA
			(cytosine-5) methyltransferases
  JOURNAL   Nat. Genet. 19 (3), 219-220 (1998)
   PUBMED   9662389
REFERENCE   2  (bases 1 to 200)
  AUTHORS   Xie,S., Okano,M. and Li,E.
  TITLE     Direct Submission
  JOURNAL   Submitted (28-MAY-1998) CVRC, Mass. Gen. Hospital, 149 13th Street,
			Charlestown, MA 02129, USA
REFERENCE   3  (bases 1 to 200)
  AUTHORS   Okano,M., Chijiwa,T., Sasaki,H. and Li,E.
  TITLE     Direct Submission
  JOURNAL   Submitted (04-NOV-1999) CVRC, Mass. Gen. Hospital, 149 13th Street,
			Charlestown, MA 02129, USA
  REMARK    Sequence update by submitter
COMMENT     On Nov 18, 1999 this sequence version replaced gi:3327977.
FEATURES             Location/Qualifiers
	 source          1..200
					 /organism="Mus musculus"
					 /mol_type="mRNA"
					 /db_xref="taxon:10090"
					 /chromosome="12"
					 /map="4.0 cM"
	 gene            1..>200
					 /gene="Dnmt3a"
ORIGIN
		1 gaattccggc ctgctgccgg gccgcccgac ccgccgggcc acacggcaga gccgcctgaa
	   61 gcccagcgct gaggctgcac ttttccgagg gcttgacatc agggtctatg tttaagtc
	  121 agctcttgct tacaaagacc acggcaattc cttctctgaa gccctcgcag ccccacagcg
	  181 ccctcgcagc cccagcctgc
//
```

A protein sequence:

```
LOCUS       DAD54807                  78 aa            linear   PLN 27-JUN-2024
DEFINITION  TPA_inf: hypothetical protein YJR107C-A [Saccharomyces cerevisiae
            S288C].
ACCESSION   DAD54807
VERSION     DAD54807.1
DBLINK      BioProject: PRJNA43747
DBSOURCE    accession BK006943.2
KEYWORDS    Third Party Data; TPA.
SOURCE      Saccharomyces cerevisiae S288C
  ORGANISM  Saccharomyces cerevisiae S288C
            Eukaryota; Fungi; Dikarya; Ascomycota; Saccharomycotina;
            Saccharomycetes; Saccharomycetales; Saccharomycetaceae;
            Saccharomyces.
REFERENCE   1  (residues 1 to 78)
  AUTHORS   Galibert,F., Alexandraki,D., Baur,A., Boles,E., Chalwatzis,N.,
            Chuat,J.C., Coster,F., Cziepluch,C., De Haan,M., Domdey,H.,
            Durand,P., Entian,K.D., Gatius,M., Goffeau,A., Grivell,L.A.,
            Hennemann,A., Herbert,C.J., Heumann,K., Hilger,F., Hollenberg,C.P.,
            Huang,M.E., Jacq,C., Jauniaux,J.C., Katsoulou,C.,
            Karpfinger-Hartl,L. et al.
  TITLE     Complete nucleotide sequence of Saccharomyces cerevisiae chromosome
            X
  JOURNAL   EMBO J. 15 (9), 2031-2049 (1996)
   PUBMED   8641269
REFERENCE   2  (residues 1 to 78)
  AUTHORS   Goffeau,A., Barrell,B.G., Bussey,H., Davis,R.W., Dujon,B.,
            Feldmann,H., Galibert,F., Hoheisel,J.D., Jacq,C., Johnston,M.,
            Louis,E.J., Mewes,H.W., Murakami,Y., Philippsen,P., Tettelin,H. and
            Oliver,S.G.
  TITLE     Life with 6000 genes
  JOURNAL   Science 274 (5287), 546 (1996)
   PUBMED   8849441
REFERENCE   3  (residues 1 to 78)
  AUTHORS   Engel,S.R., Wong,E.D., Nash,R.S., Aleksander,S., Alexander,M.,
            Douglass,E., Karra,K., Miyasato,S.R., Simison,M., Skrzypek,M.S.,
            Weng,S. and Cherry,J.M.
  TITLE     New data and collaborations at the Saccharomyces Genome Database:
            updated reference genome, alleles, and the Alliance of Genome
            Resources
  JOURNAL   Genetics 220 (4) (2022)
   PUBMED   34897464
REFERENCE   4  (residues 1 to 78)
  CONSRTM   Saccharomyces Genome Database
  TITLE     Direct Submission
  JOURNAL   Submitted (14-DEC-2009) Department of Genetics, Stanford
            University, Stanford, CA 94305-5120, USA
REFERENCE   5  (residues 1 to 78)
  CONSRTM   Saccharomyces Genome Database
  TITLE     Direct Submission
  JOURNAL   Submitted (12-APR-2011) Department of Genetics, Stanford
            University, Stanford, CA 94305-5120, USA
  REMARK    Sequence update by submitter
REFERENCE   6  (residues 1 to 78)
  CONSRTM   Saccharomyces Genome Database
  TITLE     Direct Submission
  JOURNAL   Submitted (04-MAY-2012) Department of Genetics, Stanford
            University, Stanford, CA 94305-5120, USA
  REMARK    Protein update by submitter
COMMENT     Method: conceptual translation.
FEATURES             Location/Qualifiers
     source          1..78
                     /organism="Saccharomyces cerevisiae S288C"
                     /strain="S288C"
                     /db_xref="taxon:559292"
                     /chromosome="X"
     Protein         1..78
                     /product="hypothetical protein"
     Region          1..76
                     /region_name="DUF5137"
                     /note="Protein of unknown function (DUF5137); pfam17220"
                     /db_xref="CDD:375058"
     CDS             1..78
                     /locus_tag="YJR107C-A"
                     /coded_by="complement(BK006943.2:628457..628693)"
                     /experiment="EXISTENCE:mutant phenotype:GO:0071470
                     cellular response to osmotic stress [PMID:26554900]"
                     /note="hypothetical protein; encodes new type of domain,
                     which ab initio modeling suggests is predominantly
                     alpha-helical; nonessential for growth, deletion increases
                     sensitivity to osmostress; expressed at moderate to high
                     abundance; ORF also present in strains EC1118, YJM789,
                     RM11-1a, and AWRI1631; Gln24 in S288C reference is
                     substituted with Arg in wine strain EC1118; predicted
                     S-palmitoylation site on Cys2, suggesting membrane
                     association; transcript previously mischaracterized as
                     SUT646"
                     /db_xref="SGD:S000303810"
ORIGIN
        1 mcddsydave eyyfnksvag isgqenwnkq latqvysrsl qpeilptlkp lscnkerana
       61 gkrvseeeqi ngkrkrkd
//

```