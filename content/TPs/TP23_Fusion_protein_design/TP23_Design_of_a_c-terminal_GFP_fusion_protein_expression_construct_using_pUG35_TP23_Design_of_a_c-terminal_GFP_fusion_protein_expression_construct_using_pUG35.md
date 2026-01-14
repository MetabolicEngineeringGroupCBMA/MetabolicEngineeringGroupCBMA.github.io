# **Construction of a c-terminal GFP fusion protein**
The purpose of this exercise is to construct a vector that expresses a C-terminal GFP fusion protein between *S. cerevisiae* cytochrome C and GFP. Goal is for the gene to express the cytochrome c open reading frame together with the GFP as one protein  (Fig 1).



![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.002.png)
![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.001.png)















The purpose of doing this is usually be to follow the localization of GFP inside the cell, since it is possible to see the GFP by fluorescent microscopy (Fig 2).

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.004.png)

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.003.png)







Vector selection

It is important to chose a suitable vector to propagate the fusion protein. If the vector already contain one of the fusion partners, construction is simpler. We will construct a fusion gene by amplifying the CYC1 gene by PCR and sub cloning of the CYC1 pcr product in the GFP fusion vector pUG35 (Fig 3).


![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.006.png)
![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.005.png)

The pUG35 has a MET25 (MET25-P) promoter, a multi cloning site and the GFP gene (called yEGFP3


or EGFP) in the sequence file of pUG35) shown in Fig 2. The multi cloning site (MCS) is where you can sublone genes for the expression of GFP fusion proteins. The MCS has the following available enzymes:

The pUG35 vector sequence is available from the file “pUG35.txt” that should be available in the same folder as this document. It can also be found under the genbank accession number AF298787.

**XbaI, SpeI, BamHI, SmaI, EcoRI, HindIII, ClaI** and **SalI.** Look at the Fig 3 and you will find the enzymes just before the EGFP gene.

The sequence of the CYC1 gene is available from the file CYC1.txt in this GenBank (accession V01298) or SGD (search for CYC1). The CYC1 gene does not have any of these restriction sites (you should of course check this!), so we can use any of them for sub cloning of CYC1 in gene in pUG35.

Two things are especially important to consider when designing a fusion gene.

1\. Stop codon(s)

2\. The correct reading frame

Each gene normally comes with its own stop codon. When we fuse the genes, we only need one stop codon, so that the genes are expressed as one:

Gene A 	   	**atg===taa**

Gene B (GFP) 	**atg---taa**

`                                    `**------->**

Fusion gene A-B:  	**atg===taaatg---taa**

Only first gene

is expressed.

`               `**-------------->**

Fusion gene A-B:  	**atg===atg---taa**

without stop codon

The fusion protein

is expressed.

We can easily remove the stop codon by relocating the end of the reverse primer three nucleotides upstream (to the left) of the end of the gene. Think of this as simply amplifying a gene that is three base pairs shorter than the normal.

The first task is to design PCR primers to amplify the CYC1 (accession V01298 or SGD CYC1). Remember not to include the stop codon of the gene.

The CYC1 gene has this sequence and it is 330 bp long. Make sure that you know how to find this information based on the accession number.

\>CYC1

atgactgaattcaaggccgg...gaaaaaagcctgtgagtaa

\*\*\*								---

start and stop codons are indicated by \*\*\* and ---.





Design primers:

\>fwd

atgactgaattcaagg

\>rev

ctcacaggcttttttc


**--------------->**

**||||||||||||||||**

atgactgaattcaaggccgg...gaaaaaagcctgtgagtaa

\*\*\*								---

`                       `**||||||||||||||||**

`                       `**<---------------**

Note that the reverse primer (rev) excludes the stop codon.


Now we need two restriction enzymes in order to clone the PCR product. We choose BamHI and SalI (Simply because we might have these enzymes in the freezer...).

We now add nucleotides to the primers for the restriction enzymes. If you are not sure how to do this, review the TP about tailed primers.

Add the restriction sites to the primer sequences:

\>BamHI\_fwd

GGATCCatgactgaattcaagg

\>SalI\_rev

GTCGACctcacaggcttttttc

Reading frame

We need to make sure that the CYC1 and the GFP is in the correct reading frame. Fig 2 show the reading frame of the GFP gene relative to the restriction sites.

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.008.png)

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.007.png) 

Now it is very important to define the amino acid sequence of the fusion protein.  

We know from the translation of the CYC1 gene that the CYC1 encodes a protein has 109 amino acids. This information and the sequence itself can be obtained in several ways:

1\. You can look at the GenBank file of CYC1 (V01298), the translation of the gene is available at the end of the “Features” in the sequence file.

2\. You can use an online translation tool like [http://web.expasy.org/translate](http://web.expasy.org/translate/) For this tool, it is easier only to paste the open reading frame.

3\. You can translate the gene with ApE like this:

Open the sequence file or paste the sequence in the window.

Select from start to the end of the gene (Fig 4).  You can also search for open reading frames using the ORFs>Find next function.

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.010.png)

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.012.png)

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.009.png)![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.011.png)













Select  ORFs>Translate... from the Menu, you should be seeing a window like the one in Fig 5.

Copy the translated sequence to a new text file.

We also know from the sequence file of the pUG35 (or by the same method as above) that the EGFP3 gene encodes a protein that is 238 amino acids long. Copy this sequence and place it after the CYC1 protein sequence in your text file.

Note that you may have a \* symbol in the sequence file, depending on which software you used. This indicates the stop codon. Remove this symbol (if any) from the end of the CYC1 protein sequence.

We can tell from figure 2 that the amino acids encoded by the linkers would be VDLD between the SalI site and the start codon of the EGFP3 gene. The resulting amino acid sequence should be the one indicated by figure 6.






![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.013.png)



This means that the fusion protein has to contain the sequence YLKKACEVDLDMSKGEEL. We can use this to check our result later. Make sure you really understand this step!

Put the amino acids of the linker in between the the protein sequences in your text file (Fig 7).



































![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.014.png)

Now, simulate the cloning of the PCR product in the pUG35 plasmid. It may be easier to turn the whole plasmid sequence around (view the reverse complement) before starting, since the EGFP gene is on the Crick strand and appears in the opposite direction of what we are used to.

Fig 8 shows the sequence window after the CYC1 sequence has been correctly located. Put the cursor before the A in the start codon of the CYC1 gene. Select ORFs>Find next from the Menu. This tells ApE to search for the next open reading frame that should be our fusion protein.

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.016.png)
![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.015.png)

Now the whole fusion protein should be selected. Now select ORFs>translate as before. You should see a window showing a protein sequence of **351 aminoacids**. Copy this amino acid sequence and save it in another text file.

Comparison of the sequences

Now you should compare the two aminoacid sequences (they should be the same!).

For this you can go to a web server that implements the Needleman-Wunch algorithm.

<http://www.ebi.ac.uk/Tools/psa/emboss_needle/>

Paste the translated amino acid sequence and the theoretical sequence in the other window (Fig9).


![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.018.png)
![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.017.png)

The two sequence will give the result indicated in Fig 10, 100% identity if they are the same. If not something is wrong! If they are different, you can check the details of the alignment to to find out where the error is.

![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.020.png)
![](Aspose.Words.4deb96fb-a1e3-4e89-aaa7-6730afe506be.019.png)


Use what you now know about the design of GFP fusion proteins and design a GFP fusion construct with pUG35, but with the CYC7 gene (available in the file CYC7.txt or from Genbank accession V01299) gene instead and use the restriction enzymes **XbaI** and **ClaI**.

**Question 1:**

The cSEGUID of the plasmid starts with **n51k4\_og**.  What are the last four characters in the cSEGUID of the plasmid.

**Question 2:**

What is the size of the fusion protein (number of amino acids)?

