# **Automatic assembly of PCR products with Web PCR**

Assembly of PCR products from the sequences of primers and template sequence is possible using any sequence editor (like ApE), but it is tedious and error prone.

There is an on-line web service called WebPCR that can do this for you. This service can predict the sequence of the PCR products given the sequence of the primers and of the template.

Go the web page: [http://pydna.pythonanywhere.com](http://pydna.pythonanywhere.com/). You should see a window like Fig 1.

![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.002.png)*
![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.001.png)

Click on the **PCR simulator** button You should now see a site similar to the one in Fig 2.

![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.004.png)
![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.003.png)

The window accepts pasted sequences in **FASTA** or **Genbank** formats. The last of the sequences is assumed to be the template, all other sequences are assumed to be primers:

This means that you can add more than two primers if you like. Delete all text in the window of Web PCR and paste the following three sequences in the window. The sequences in are also available in the “primers\_and\_template\_sequences.txt” file that should be present in the same folder as this document.

\>2\_3CYC1clon

CGATGTCGACTTAGATCTCACAGGCTTTTTTCAAG

\>1\_5CYC1clone

GATCGGCCGGATCCAAATGACTGAATTCAAGGCCG


LOCUS       YJR048W\_\_Chr\_10\_        2330 bp ds-DNA     linear       05-JUN-2012

DEFINITION  .

ACCESSION   

VERSION     

SOURCE      .

`  `ORGANISM  .

COMMENT     >YJR048W  Chr 10   from 525335 to 527664  

COMMENT     ApEinfo:methylated:1

FEATURES             Location/Qualifiers

`     `misc\_feature    959..1003

`                     `/label=New Feature

`     `misc\_feature    1327..1372

`                     `/label=New Feature(1)

ORIGIN

`        `1 GAGGCACCAG CGTCAGCATT TTCAAAGGTG TGTTCTTCGT CAGACATGTT TTAGTGTGTG

`       `61 AATGAAATAG GTGTATGTTT TCTTTTTGCT AGACAATAAT TAGGAACAAG GTAAGGGAAC

`      `121 TAAAGTGTAG AATAAGATTA AAAAAGAAGA ACAAGTTGAA AAGGCAAGTT GAAATTTCAA

`      `181 GAAAAAAGTC AATTGAAGTA CAGTAAATTG ACCTGAATAT ATCTGAGTTC CGACAACAAT

`      `241 GAGTTTACCA AAGAGAACAA TGGAATAGGA AACTTTGAAC GAAGAAAGGA AAGCAGGAAA

`      `301 GGAAAAAATT TTTAGGCTCG AGAACAATAG GGCGAAAAAA CAGGCAACGA ACGAACAATG

`      `361 GAAAAACGAA AAAAAAAAAA AAAAACACAG AAAAGAATGC AGAAAGATGT CAACTGAAAA

`      `421 AAAAAAAGGT GAACACAGGA AAAAAAATAA AAAAAAAAAA AAAAAAAGGA GGACGAAACA

`      `481 AAAAAGTGAA AAAAAATGAA AATTTTTTTG GAAAACCAAG AAATGAATTA TATTTCCGTG

`      `541 TGAGACGACA TCGTCGAATA TGATTCAGGG TAACAGTATT GATGTAATCA ATTTCCTACC

`      `601 TGAATCTAAA ATTCCCGGGA GCAAGATCAA GATGTTTTCA CCGATCTTTC CGGTCTCTTT

`      `661 GGCCGGGGTT TACGGACGAT GGCAGAAGAC CAAAGCGCCA GTTCATTTGG CGAGCGTTGG

`      `721 TTGGTGGATC AAGCCCACGC GTAGGCAATC CTCGAGCAGA TCCGCCAGGC GTGTATATAT

`      `781 AGCGTGGATG GCCAGGCAAC TTTAGTGCTG ACACATACAG GCATATATAT ATGTGTGCGA

`      `841 CGACACATGA TCATATGGCA TGCATGTGCT CTGTATGTAT ATAAAACTCT TGTTTTCTTC

`      `901 TTTTCTCTAA ATATTCTTTC CTTATACATT AGGACCTTTG CAGCATAAAT TACTATACTT

`      `961 CTATAGACAC ACAAACACAA ATACACACAC TAAATTAATA ATGACTGAAT TCAAGGCCGG

`     `1021 TTCTGCTAAG AAAGGTGCTA CACTTTTCAA GACTAGATGT CTACAATGCC ACACCGTGGA

`     `1081 AAAGGGTGGC CCACATAAGG TTGGTCCAAA CTTGCATGGT ATCTTTGGCA GACACTCTGG

`     `1141 TCAAGCTGAA GGGTATTCGT ACACAGATGC CAATATCAAG AAAAACGTGT TGTGGGACGA

`     `1201 AAATAACATG TCAGAGTACT TGACTAACCC AAAGAAATAT ATTCCTGGTA CCAAGATGGC

`     `1261 CTTTGGTGGG TTGAAGAAGG AAAAAGACAG AAACGACTTA ATTACCTACT TGAAAAAAGC

`     `1321 CTGTGAGTAA ACAGGCCCCT TTTCCTTTGT CGATATCATG TAATTAGTTA TGTCACGCTT

`     `1381 ACATTCACGC CCTCCTCCCA CATCCGCTCT AACCGAAAAG GAAGGAGTTA GACAACCTGA

`     `1441 AGTCTAGGTC CCTATTTATT TTTTTTAATA GTTATGTTAG TATTAAGAAC GTTATTTATA

`     `1501 TTTCAAATTT TTCTTTTTTT TCTGTACAAA CGCGTGTACG CATGTAACAT TATACTGAAA

`     `1561 ACCTTGCTTG AGAAGGTTTT GGGACGCTCG AAGGCTTTAA TTTGCAAGCT TCGCAGTTTA

`     `1621 CACTCTCATC GTCGCTCTCA TCATCGCTTC CGTTGTTGTT TTCCTTAGTA GCGTCTGCTT

`     `1681 CCAGAGAGTA TTTATCTCTT ATTACCTCTA AAGGTTCTGC TTGATTTCTG ACTTTGTTCG

`     `1741 CCTCATGTGC ATATTTTTCT TGGTTCTTTT GGGACAAAAT ATGCGTAAAG GACTTTTGTT

`     `1801 GTTCCCTCAC ATTCCAGTTT AGTTGTCGAC TGATACTGTT AATAAACTCA TCGGGCGAGG

`     `1861 CTTCCACGGT TGGAAAAGCA TATGGGCTGG CGCATATGGT TATAAAATCA CCTTTTTGCA

`     `1921 ATTCAATTCT ATCTTTCCCA TCAAAAGCCG CCCATGCTGG AGCCCTTGAC TTCATCGAGA

`     `1981 CTTTCACTTT TAAATTTATA CTTTCTGGTA AGATGATGGG TCTGAAACTC AATGCATGTG

`     `2041 GACAAATGGG TGTTAAAGCG ATTGCATTGA CGGTTGGGCA TACCAATGAC CCACCTGCAC

`     `2101 TCAAAGAATA GGCCGTGGAC CCAGTCGGAG TAGCAGCAAT CAGTCCGTCC GCCTGCGCAA

`     `2161 CGGTCATTAA TGAGCCGTCA CCATACAATT CTAACATGGA TAGAAAAGGA CTTGGACCAC

`     `2221 GATCGATGGT CACTTCGTTC AAAATGTGGT GTGTGCTTAG TTTTTCCACC ACACATATTT

`     `2281 TCTTCCCCGT GTTTGGGTCT ACTTCAGGGC GGTGTCTACG ATAAATTGTG

//

click “Run simulation” you should now get the following output below the window (next page):

![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.006.png)
![](Aspose.Words.4251c487-aece-4357-8a81-438040fec7ac.005.png)

The simulation found one potential PCR product of 359 bp. The report has five parts. The first part (below) tells us general things about the template molecule (name, size and if it is linear or circular).

pydna 4.0.0a10

Template YJR048W\_\_Chr\_10\_ 2330 nt linear:

1\_5CYC1clone anneals forward (--->) at 1019

2\_3CYC1clon anneals reverse (<---) at 1308

Number of products formed: 1

\--------------------------------------------------------------------------------

` `The second part gives us the primers and the template PCR product in FASTA format.

\>1\_5CYC1clone

GATCGGCCGGATCCAAATGACTGAATTCAAGGCCG

\>2\_3CYC1clon

CGATGTCGACTTAGATCTCACAGGCTTTTTTCAAG

\>YJR048W\_\_Chr\_10\_

GAGGCACCAGCGTCAGCATTTT...GATAAATTGTG

\----

The third part is a figure showing how the primers anneal on the template.

\----

`               `5AATGACTGAATTCAAGGCCG...CTTGAAAAAAGCCTGTGAG3

`                                       `|||||||||||||||||||

`                                      `3GAACTTTTTTCGGACACTCTAGATTCAGCTGTAGC5

5GATCGGCCGGATCCAAATGACTGAATTCAAGGCCG3

`                `||||||||||||||||||||

`               `3TTACTGACTTAAGTTCCGGC...GAACTTTTTTCGGACACTC5

\----

The fourth part has the PCR product in FASTA format. The product is given in the direction of the primers.

\----

\>359bp\_PCR\_prod

GATCGGCCGGATCCAAATGACTGAATTCAAGGCCGGTT...AGTCGACATCG

\----

The fifth an final part suggests PCR programs using either Taq polymerase or Pfu-Sso7d (such as [PfuX7](https://www.ncbi.nlm.nih.gov/labs/pmc/articles/PMC2847956) or the commercial [Phusion](https://www.thermofisher.com/order/catalog/product/F-530XL) for example.

\----

Taq DNA polymerase

|95°C|95°C               |    |tmf:62.4

|\_\_\_\_|\_\_\_\_\_          72°C|72°C|tmr:59.1

|3min|30s  \ 48.7°C \_\_\_\_\_|\_\_\_\_|45s/kb

|    |      \\_\_\_\_\_\_/ 0:30|5min|GC 47%

|    |       30s         |    |48bp

Pfu-Sso7d DNA polymerase

|98°C|98°C               |    |tmf:56.7

|\_\_\_\_|\_\_\_\_\_          72°C|72°C|tmr:53.8

|30s |10s  \ 56.8°C \_\_\_\_\_|\_\_\_\_|15s/kb

|    |      \\_\_\_\_\_\_/ 0:10|5min|GC 47%

|    |       10s         |    |48bp

**Question 1:**

Use the sequences in the file “**primers\_and\_template\_sequences2.txt**” file that should be present in the same folder as this document.

Check the SEGUID of the **PCR product**.

The first five characters of the SEGUID are **ifnuA**

What are the last five?




**Question 2:**

This is an individual question for each student. Follow this [link](https://docs.google.com/spreadsheets/d/1OOtGomVp87Gkpmb7xopV3nXIOigW5tXQo6ZxHf5ziTY/edit?usp=sharing) that points to a Google Spreadsheet.   You should find your name in the leftmost column. Three columns called **primer1,2** and **template** contains DNA sequences representing primers and a template. Your task is to use the WebPCR service to simulate the PCR. Put your result  in the indicated cell for forward primer (**product**). **Please answer with a raw DNA sequence as indicated for the first example student "*Max Maximus*"**. This will speed up correction. If your name is **\*not\*** in the list, please inform your instructor.




© Björn Johansson 2020
