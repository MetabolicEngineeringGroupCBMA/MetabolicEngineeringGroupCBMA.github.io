![[in silico assembly of pYPKa_A_ATF1-20240926073427367.png]]



The pYPKa_A_ATF1 is a cloning vector which has the *S. cerevisiae* alcohol acetyltransferase gene *[ATF1/YOR377W](https://www.yeastgenome.org/locus/S000005904)* gene, but no promoter or terminator.

The purpose of this plasmid is to serve as template for a subsequent PCR reaction.


![](ATF1.png)

The plasmid is made by cloning a PCR product containing the *ATF1* gene into the *AjiI* restriction site of the pYPKa plasmid using the AjiI restriction enzyme and DNA ligase.

![[in silico assembly of pYPKa_A_ATF1-20240924080715125.png]]

The  *AjiI* restriction site is blunt, so we do **not** need to digest the PCR product as has blunt ends already.

Use the following in order to assemble the sequence for the **pYPKa_A_ATF1** plasmid *in-silico*:

## 1. PCR simulation

1. Copy the sequence the sequence of the *ATF1* gene ([CP046095.1](https://www.ncbi.nlm.nih.gov/nucleotide/CP046095.1?report=genbank&log$=nuclalign&blast_rank=1&RID=KDUDWCZH016&from=1040471&to=1042048) ) from Genbank. This is the template for the PCR simulation. Be careful to copy the complete [[GenBank#Genbank format\|Genbank]] sequence.
2. The two primer sequences below (1795 & 1732), used to amplify the ATF1 gene from chromosomal DNA.

```
>1795_ATF1f CP072089 1046219 1047796
gcaataATGGGTAATGAAATCGATGAGAAAAATCA
	
>1732_ATF1r CP072089 1046219 1047796
TTAAGGGCCTAAAAGGA
```

Use the [WebPCR](https://pydna.pythonanywhere.com/pcr) tool to simulate the PCR reaction using the primer sequences and the *ATF1* sequence from GenBank.
Place the primer sequences before the *ATF1* gene as indicated in the figure below.

![[in silico assembly of pYPKa_A_ATF1-20240709175312224.png]]
Click "submit" to perform the simulation. the result should look like this:

![[in silico assembly of pYPKa_A_ATF1-20240926064924447.png]]
The last sequence is the PCR product. The PCR product sequence should be 1587 bp long:

![[in silico assembly of pYPKa_A_ATF1-20240926072124376.png]]

## 2. *in-silico* cloning

Get the pYPKa sequence [file](https://github.com/MetabolicEngineeringGroupCBMA/YeastPathwayKit/blob/master/sequences/pYPKa.gb) and open it in ApE. You can do this by saving the file to your computer and
dragging the sequence file to the empty ApE window. See the result below. The sequence should have 3128 bp.

 ![[in silico assembly of pYPKa_A_ATF1-20240709173627486.png]]

Find  The **[AjiI](http://rebase.neb.com/rebase/enz/AjiI.html)** has the same specificity as the enzymes ** [BtrI](http://rebase.neb.com/rebase/enz/BtrI.html) ** or **[BmgBI](http://rebase.neb.com/rebase/enz/BmgBI.html)**.
Use the Enzymes>Enzyme selector option and try to find the AjiI restriction site.
You can also use the Edit>Find or CTRL-F search to find the recognition sequence of the enzyme (CACGTC).

If **AjiI** is not available in the enzyme selection of ApE, try to find  **BtrI** instead.

Paste the PCR product sequence at the cut site of the pYPKa. See figure below.

![[in silico assembly of pYPKa_A_ATF1-20240709180601962.png]]

> [!IMPORTANT]
> Paste only the DNA sequence of the PCR product, do not include the FASTA header.



## 3. Analyze resul

Calculate the **size** and complete **seguid checksum** of the resulting plasmid.

The expected size is 4715 Kb and the short seguid checksum is `cdseguid=EsiXAn`

The seguid checksum is available in ApE by clicking on the finger print button (see figure above).

Compare your result with that of your colleagues. Save the new sequence file on your computer under the name **pYPKa_A_ATF1.gb**.

You can continue to the assembly of the *AFT1* TU-vector [[in silico assembly of pTA1_TDH3_ATF1_PGI1\|pTA1_TDH3_ATF1_PGI1]].
