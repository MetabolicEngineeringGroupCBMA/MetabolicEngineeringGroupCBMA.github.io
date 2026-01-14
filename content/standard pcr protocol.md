# Standard PCR protocol

This is a compilation of general guidelines for PCR. Most of it was lifted from the FERMENTAS website many years ago.

| Reagent stock      	  |	Final concentration |
|-------------------------|---------------------|
|Sterile deionized water  |	-                   |
|10X Taq buffer           |	1X                  |
|2-10 mM dNTP mix         |	0.2 mM of each      |
|Taq DNA Polymerase       |	1.25 U / 50 µl      |
|25-50 mM MgCl2           |	2 mM                |
|Primer I				  |	0.5 µM              |
|Primer II				  |	0.5 µM              |
|Template DNA			  |	10 pg-1 µg          |

Note the concentrations of the stock solutions.
## Mastermix

Normally, we do not prepare the PCR mix for each PCR, but we use a frozen [[2x PCR mastermix]] with 2x concentration.
This means that you take for example 25 µL mix to a 50 µL reaction and then add primers, template and water to 50 µL.
This reduces pipetting errors and increases consistency.

### Mastermix with Phusion DNA polymerase

For 1400 µL (fits in one 1.5mL Eppendorf tube!):

|Component                  | Volumes |
|---------------------------|---------|
|H2O                        | 672.0   |
|5xHF Buffer w 7.5mM MgCl2  | 560.0   |
|dNTPs(10 mM)               | 56.00   |
|DMSO(100%)                 | 84.00   |
|Phusion (2U/µL)            | 28.00   |

See this spreadsheet [PhusionMasterMix2x](PhusionMasterMix2x.ods)

We add 3% DMSO for safe measure.

### Mastermix with homemade Taq DNA polymerase

For 1000 µL :

|Component             | Volumes |
|----------------------|---------|
|H2O                   | 686     |
|Taq buffer w NH4SO4   | 280     |
|MgCl2(25 mM)          | 224     |
|dNTPs(10 mM)          | 56      |
|DMSO(100%)            | 84      |
|Taq (1U/µL)           | 70      |

See this spreadsheet [TaqMasterMix2x](TaqMasterMix2x.ods)

We add 3% DMSO for safe measure.

## PCR program

If you have the sequence of the template and primers, [pydnaweb](https://pydnaweb.streamlit.app)
can simulate the PCR and suggest a PCR program.

Generally, the rate of DNA synthesis by Taq DNA Polymerase and Pfu DNA
Polymerase is highest at 70-75°C. As a rule, the extension step with Taq
DNA Polymerase is 1 min at 72°C for PCR products up to 2 kb.

For larger products, the extension time can be prolonged by 1 min/kb. Since Pfu DNA Polymerase
exhibits lower extension rate, an extension step of 2 min/kb at 72°C is
recommended.

Melting temperature (Tm):

Melting temperatures for oligonucleotides can be calculated from simple formulae
(e.g. Tm = 2[A+T] + 4[G+C]), or determined by software programs developed
specifically for this purpose. It is unclear which is the best method to mos
accurately calculate Tm. Optimal annealing temperature (Ta):

A general rule of thumb is to use a temperature approximately 5 °C lower than
the Tm of the primers. Alternatively, there are more complex equations to
calculate Ta (Rychlik et al., Nucleic Acids Research 18:6409-6412).


## Stock solutions:

Primers are diluted to 100µM stock if nothing else is specified.
You should not use the stocks directly, make a 10 times dilution for yourself.
Make sure to

MgCl2 stock solutions are typically 25mM or 50mM.

Primers: 	10uM (10x dilution of the MWG standard conc)
dNTPs		1 mM (10x dilution of the normal stock)
[rel://protocols/Screenshot-Java-applet for PCR or qPCR reaction mixture setup - Mozilla Firefox.png]

Volume calculators: http://primerdigital.com/Tools/ReactionMixture.html
Troubleshoot PCR:    http://www.med.yale.edu/genetics/ward/tavi/Trblesht.html

## Additives

may improve results:
- DMSO (up to 10%)
- Detergents (NP40, Triton X-100, Tween® 20) up to 1%

See links below for more suggestions.

See [here](http://bitesizebio.com/24/pcr-problems-try-an-additive/)
and [here](http://bitesizebio.com/2592/better-than-betaine-pcr-additives-that-actually-work/)



## Buffer

Fermentas (now ThermoFisher) describe a buffer that works very well in our hands. The recipe is taken
from this [website](https://www.thermofisher.com/order/catalog/product/B33).

10x Taq Buffer with (NH4)2SO4 w/o MgCl2:
- 750 mM Tris-HCl (pH 8.8 at 25°C)
- 200 mM (NH4)2SO4
- 0.1% (v/v) Tween 20

This buffer can be prepared in this way (100 mL):

1. Add 9.0855 g Tris-Base (MW 121.14) to about 75 mL of the purest available water and a magnetic stirrer bar.
2. Set pH to 8.8 with concentrated HCl. Set the pH before the addition of the (NH4)2SO4.
3. Add 2.6428 g (NH4)2SO4 (MW 132.14) to the solution and mix.
4. Transfer to a 100mL volumetric flask and adjust the volume.
5. Add 100µL or 90 mg [Tween 20](https://en.wikipedia.org/wiki/Polysorbate_20)
6. Mix, aliquot and freeze. Autoclaving is not needed.

This buffer has no MgCl2.


## MgCl2

Mix 2.0331 g MgCl2 (MgCl2x6H2O, MW 203.31g/mol) with 50 mL of the purest available water. The final concentration
is 200 mM.
