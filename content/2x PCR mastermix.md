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

###  1.5x Green PCR mastermix (mastermix with PCR compatible loading buffer)

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

Since we make our own mastermix, we need a standardized test. We use the following mix:

- 78 µL H2O
- 10 µL Primer 19
- 10 µL Primer 18
- 2 µL Chromosomal DNA from yeas

The primers amplify a 1288 bp PCR product from the DFR1 locus in *S. cerevisiae*
using this program consisting of initial denaturation for 4 min at 94 °C, followed by 30 cycles of 94 °C for 30s, 50 °C for 30s, and 72 °C for 45 s, and a final extension at 72 °C for 5 min. [Source](https://link.springer.com/book/10.1007/978-1-0716-3358-8)

```
| 94.0°C  |94.0°C                 |      |
|_________|_____          72.0°C  |72.0°C|
| 04min00s|30s  \         ________|______|
|         |      \ 50.0°C/ 0min45s| 5min |
|         |       \_____/         |      |
|         |         30s           |      |
```

This PCR reaction is very robust and gives a high yield.

Primers
- 19_D-DFR1 GACTCAGACAGGTTGAAAAGAAGAC
- 18_A-DFR1 CAAAGGTTTGGTTTTCAGTTAAGAA