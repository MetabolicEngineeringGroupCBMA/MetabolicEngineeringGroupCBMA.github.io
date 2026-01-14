![[Microwave Yeast Colony PCR_002.png]]

This protocol is based on the protocol specified by Michael Lisby at University of Copenhagen [here](http://www1.bio.ku.dk/english/research/fg/transkription/resources/protocols/colonypcr/). The advantage of this protocol is that it is fast and simple, the disadvantage might be that it seems less efficient for PCR products over 2000 bp. This protocol works best with fresh yeast on plates. You need a microwave oven for this protocol.

1. Book the PCR machine.

2. Prepare a PCR mix for the number of clones you have plus two negative (empty strain and no cells) and one positive control (if possible) and one extra for safe measure. The total volume of the PCR mixture should be 20 µL. We disregard the volume of the yeast cells, since it should be very small in comparison.

        for example, if you have ten clones to test,
        we make a mix for 13 reactions if we have
        a positive control.

        2x PCR mastermix        10 * 13 = 130
        primer1 (10 µM)         2  * 13 = 26
        primer2 (10 µM)         2  * 13 = 26
        H2O                     6  * 13 = 78

    Leave the PCR mixture on ice.

3. Program the PCR machine. It can be an advantage to add a 10 min pause at 95°C to further lyse the cells. If you have the sequences of the primers and the template, use the [WebPCR](https://pydna.pythonanywhere.com) simulator and use the program that is given, but use 35 cycles instead of 30.

        For example:

        95°C	 10 min

        35 cycles of:

            95°C	 Denaturation 30 sec
            55°C	 Annealing    30 sec (adjust Annealing temperature and extension time according to results from webpcr)
            72°C	 Extension    30 sec

        Room temperature (The 4-12°C hold is not necessary)

It is best to use hot-start PCR, so turn the machine on and pause in the initial denaturation step.
Some PCR tubes of lower quality has a tendency to pop open while adding them to a hot PCR block.
In this case a normal cold-start is preferred.

3. Using the tip of a yellow or white pipette tip, transfer a small amount of cells to the inside of a PCR tube.

4. Microwave for 2 min at max power.

5. Place tubes on ice to cool down.

6. Add 20 µL of the reaction mix to each tube. Be careful to switch pipette tip between each addition. The negative control should be the tube that you prepare last.

7. Store tubes at -20°C or Run PCR directly  .

#### Extra

The mastermix should contain a thermostable polymerase with a compatible buffer, dNTPs and Mg2+ at two times the final desired concentration

On interesting variation is the The Blackburn: Yeast Colony PCR v2.0. This [protocol](http://openwetware.org/wiki/Blackburn:Yeast_Colony_PCR_v2.0) use 20 mM NaOH and Qiagen Q-buffer which mainly contains Betaine (Trimethylglycine)

Betaine can be bought from [Sigma](http://www.sigmaaldrich.com/catalog/ProductDetail.do?N4=B0300|SIGMA&N5=SEARCH_CONCAT_PNO|BRAND_KEY&F=SPEC), 1.5 mL cost 28.50 euros and is 5M which is 5x.

This quantity is good for 1500 * 5 = 7500 µL PCR mix or 7500/20  = 375.0 twenty µL PCR reactions.
This means 28.50/375 = 0.076 or 7.6 cents per PCR reaction which might be OK.

This [page](http://www.staff.uni-mainz.de/lieb/additiva.html) has a list of PCR adjuvants with references.

Commonly used PCR adjuvants are:
    5% Glycerol
    5% DMSO
    0.8 mg/mL BSA
    [T4 Gene 32 Protein](http://www.sigmaaldrich.com/catalog/product/roche/t4gene32ro?lang=pt&region=PT)

### Note

Colony PCR from yeast is a notoriously fickle protocol which can easily be seen by the many variations available by searching the internet.
It seems many users have to tweak the protocol for it to work. Test the protocol with a positive and negative control if you can.
This protocol is probably one of the quickest, but works best with short products.
If this does not work, consider protocols involving NaOH or enzymatic degradation of the cell wall.

Pereira, Humberto, Paulo César Silva, and Björn Johansson. 2023. “Bacteria and Yeast Colony PCR.” _Methods Mol. Biol._ 2967:209–21. [https://doi.org/10.1007/978-1-0716-3358-8_17](https://doi.org/10.1007/978-1-0716-3358-8_17).
