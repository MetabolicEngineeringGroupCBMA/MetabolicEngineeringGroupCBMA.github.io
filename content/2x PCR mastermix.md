### 2x PCR mastermix

Using a PCR master-mix saves time and improves PCR reproducibility, especially if many reactions are prepared. For a standard PCR reaction, half of the final volume should be
used, for example 25 µL 2x PCR mastermix for a 50 µL PCR reaction. Scale up or down as needed.

| Component  | µL  | stock | 2xPCR mastermix | final concentration in PCR reaction |
| ---------- | --- | ----- | --------------- | ----------------------------------- |
| Water      | 16  | -     | -               | -                                   |
| Buffer(xC) | 5   | 10x   | 2x              | 1x                                  |
| MgCl2(mM)  | 2   | 50 mM | 4 mM            | 2 mM                                |
| dNTPs(mM)  | 1   | 10    | 0.4             | 0.2                                 |
| Taq        | 1   | 100%  | 5.0%            | 2.5%                                |
| Total      | 25  | -     | -               | -                                   |

See [[standard pcr protocol]].

### 1.5x Green PCR mastermix (mastermix with PCR compatible loading buffer)

The 2xPCR mastermix can be combined with a PCR compatible loading buffer such as the in described in the table below. This saves time if you have many samples as they can be loaded directly on a gel. Use 33 µL of the 1.5x Green PCR mastermix for a 50 µL PCR reaction. Scale up or down as needed.

| Component                                                       | µL  |
| --------------------------------------------------------------- | --- |
| 2x PCR mastermix                                                | 25  |
| [[6x DNA loading buffer\|6 x DNA loading buffer (PCR compatible)]] | 8   |
| Total                                                           | 33  |

### For MEC lab members:

This [google sheet](https://docs.google.com/spreadsheets/d/1KWIgyq6alo-SgLN6TYQieGoHQNPxkIb1-JcRGnsbUoc/edit#gid=849990250) contains the recipe above. Create a new tab named after the date of preparation in [ISO 8601](https://xkcd.com/1179) format.
Copy paste an old recipe and modify if necessary.

### Testing

Since we make our own master mix, we need a standardized test mix. The primers 18 and 19 amplify a 1288 bp PCR product from the DFR1 locus in _S. cerevisiae_. This PCR reaction is very robust and gives a high yield. We use the following mix:

- 78 µL H2O
- 10 µL Primer (10 µM) `19_D-DFR1 GACTCAGACAGGTTGAAAAGAAGAC`
- 10 µL Primer (10 µM) `18_A-DFR1 CAAAGGTTTGGTTTTCAGTTAAGAA`
- 2 µL Chromosomal DNA from _S. cerevisiae_

Add 5 µL of the test mix to  5 µL of 2x master mix and run the PCR program below: [Source](https://link.springer.com/book/10.1007/978-1-0716-3358-8)

```
Taq (rate 30 nt/s) 35 cycles             |1288bp
95.0°C    |95.0°C                 |      |Tm formula: Biopython Tm_NN
|_________|_____          72.0°C  |72.0°C|SaltC 50mM
| 03min00s|30s  \         ________|______|Primer1C 1.0µM
|         |      \ 55.0°C/ 0min39s| 5min |Primer2C 1.0µM
|         |       \_____/         |      |GC 40%
|         |         30s           |      |4-12°C
```
