# 6 x DNA loading buffer (PCR compatible)

## Use

Add 1/6 volume of this DNA Loading buffer to your DNA sample, for example 5 µL DNA sample and 1 µL loading buffer.

Often we have more concentrated DNA solutions as for example a normal DNA miniprep of a plasmid where about 2 µL DNA
sample is enough for checking size and integrity. If you have many samples, mix one volume (for example 10 µL ) 6 x DNA loading buffer
with two volumes of water (for example 20 µL ). Mix well and put 4 µL drops of the mixture on a piece of Parafilm and mix each drop with 2 µL of DNA sample.
This mixture will have the right fraction of loading buffer.

## Preparation
The table below contain the components of a 6x loading buffer used in the lab. It has two colors
one bluish that migrates slowly and one yellow that migrates rapidly. This loading buffer should be
compatible with PCR (see below). Note that the buffer should contain either Orange G *or* Tartrazine
as the yellow color. Orange G is preferred since it migrates faster.

| Component                     |Quantity |Concentration (w/v)| Final concentration       |Function       |
| ----------------------------- |---------|------------------ | ------------------------- |---------------|
| FICOLL 400 (powder)           | 6.25 g  | 12 %              | 2.0 %                     | Density       |
| Xylene Cyanol FF (powder)     | 7.5 mg  | 0.015 %           | 0.0025 %                  | Blue color    |
| VAHINE yellow (Tartrazine)    | 900 µL  | 1.8 %             | 0.30 %                    | Yellow color  |
| Orange G (1% w/v)             | 7.2 mL  | 0.144 %           | 0.024 %                   | Orange color  |
| Water                         | -       | to 50 mL          |                           | -             |
| Total                         | 50 mL   |                   |                           |               |


Recipe for 50 mL 6x DNA loading buffer:

- add 6.25g [FICOLL 400](https://www.sigmaaldrich.com/catalog/product/sigma/f2637) powder to a new 50 mL FALCON tube.
- add [[ddH2O]] to about 30 mL, shake to dissolve. This may take time, heating the tube in a water bath helps.
- add 7.5 mg Xylene Cyanol FF powder
- add 7.2 mL Orange G (1% w/v) *OR* 900 µL of VAHINE yellow contains [Tartrazine](http://en.wikipedia.org/wiki/Tartrazine)
- add water to 50 mL

The resulting solution is about the same colour as the GoTaq green flexi buffer commercialized
by [Promega](https://worldwide.promega.com/products/pcr/endpoint-pcr/gotaq-reaction-buffers/?catNum=M7911).
The gel below shows GoTaq green flexi buffer loaded on gel.


![[gotaq.jpg]]


This loading buffer is be compatible with PCR, add it to 16% (v/v) of the final PCR (8 µL in a 50 µL reaction) volume. This can be added to the [[2x PCR mastermix]].


The yellow food coloring contain Tartrazine (E102). In this case, exact concentration
is not known, but could be measured using a spectrophotometer at the absorption
maximum of 472 nm. The molar absorptivity of Tartrazine at 472 nm is 20,330 L mol-1 cm-1.


### Development

#### FICOLL 400 (Density)

From invitrogens website I found the following information:

    Xylene Cyanol (0.02%), Tartrazine and Ficoll (2.5%) do not inhibit this enzyme (recombinant Taq).

The information was avaliable thorugh this [link](http://www.invitrogen.com/site/us/en/home/Products-and-Services/Applications/PCR/pcr-enzymes-master-mixes/taq-dna-polymerase-enzymes/taq_dna_polymerase.html).

I could not find information for PHUSION, but I assume this enzyme is not more sensitive.

This suggests that 2.5% ficoll could be added to a PCR reaction.

Kramer 2001 suggests to add 0.5 - 1% Ficoll 400. Surpisingly they refer to v/v:

    add Ficoll 400 to a final concentration of 0.5% to 1% (v/v)

Kramer, M. F., & Coen, D. M. (2001). Enzymatic amplification of DNA by PCR: standard procedures and optimization. Current Protocols in Molecular Biology / Edited by Frederick M. Ausubel... [et Al.], Chapter 15, Unit 15.1.

#### Xylene Cyanol FF (Blue)

PCR mastermix can tolerate 0.0025% Xylene Cyanol FF in the final solution.
For example, commercial https://international.neb.com/products/m0271-quick-load-taq-2x-master-mix#Product Information
yields 0.0025% XyleneCyanol FF in the final 1x PCR mixture:

[![[1X_Quick-Load_Taq_Master_Mix.png]]](M0271Datasheet-Lot0211206.pdf)

The final loading buffer should have 0.0025% (w/v) dye.
The loading buffer is 6x concentrated, so the loading buffer should have 0.0025 * 6 = 0.015% (w/v).
If we assume a density of 1 g/mL (the final buffer is denser), we should add (0.015/100) * 50000 = 7.5 mg of dye to 50 mL.

#### Orange G

Commercial 2X Quick-Load Taq Master Mix has 0.024% Orange G (see above).

#### VAHINE yellow (Tartrazine)

[Hoppe 1992](https://www.ncbi.nlm.nih.gov/pubmed/1515133) tests various dyes for their compatibility with PCR.
This paper is old and I have not been able to find any version of it on-line. However, a more recent paper refer
to it, [Prigge 2001](https://www.ncbi.nlm.nih.gov/pubmed/11402159) and they make the following claim:

> To facilitate higher throughput PCR mapping, loading dyes and sucrose
> were included in the reaction mixtures (Hoppe et al., 1992). PCR reactions
> contained 50 mM KCl, 10 Tris-HCl, pH 8.3, 1 mM MgCl2, 0.1 g/L BSA, 12% sucrose,
> 0.1% Triton X-100, 0.2 mM cresol red, 0.3% yellow food coloring (McCormick and Co., Inc., Hunt Valley, MD),
> 125 M each dNTP, 250 nM each primer, and 0.1 U/ L Taq polymerase.

The [[mccormick-food-coloring.jpg|McCormick food coloring]] seem equivalent to the
VAHINE available in Portugal (see above). In our
recipe the final concentration is (0.9 mL / 50 mL ) / 6 = 0.3 % (v/v).


### Misc

VAHINE food coloring comes in a package with blue, red and yellow. It has the following components:

| color | component | absorption maximum |
| ---- | ---- | ---- |
| blue | [E133  Brilliant Blue FCF](http://en.wikipedia.org/wiki/Brilliant_Blue_FCF) |  |
| red | [E122  Carmoisine](http://en.wikipedia.org/wiki/Azorubine) | 510 nm |
| yellow | [E102  Tartrazine](http://en.wikipedia.org/wiki/Tartrazine) |  |

### Links


- http://www.wendychao.com/science/protocols/loading_buffer/
- http://www.protocol-online.org/biology-forums-2/posts/12397.html
- http://www.geneticorigins.org/pv92/recipes2.htm
- https://www.researchgate.net/post/Which_dye_doesnt_inhibit_PCR_reaction
