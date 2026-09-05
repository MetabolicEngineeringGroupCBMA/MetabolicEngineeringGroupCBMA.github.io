---
publish: true
aliases: [gel]
---

## Purpose

Agarose gel electrophoresis separates DNA fragments based on size. It is commonly used to verify:

- PCR amplification products
- Restriction enzyme digestions
- Plasmid preparations
- DNA fragment sizes

DNA migrates through agarose toward the positive electrode because DNA is negatively charged. Smaller fragments move faster than larger ones.
# Preparing DNA Samples for Loading

DNA samples should be mixed with a **loading buffer** before loading into the gel in most cases.

Loading buffer serves two purposes:

1. **Adds density** so the sample sinks into the well
2. **Contains tracking dyes** so migration during electrophoresis can be monitored

Common dyes:

- Xylene cyanol FF (light blue color)
- Bromophenol blue (dark blue color)
- Orange G

![[GEL.png]]

The dye migration roughly corresponds to DNA fragment sizes depending on agarose concentration.

We use this buffer that we make ourselves [[6x DNA loading buffer]] it has Xylene cyanol FF and Orange G
but no Bromophenol blue as this dye has a tendency to hide some DNA bands. Our loading buffer
is also PCR compatible, which means that it can be added to the PCR mix prior to PCR.

You can add loading buffer to PCR by substituting some of the water added. For each 100 µL of
PCR reaction mix, substitute 17 µL of water with [[6x DNA loading buffer]].

You can also prepare [[2x PCR mastermix]] with loading buffer. For each 100 µL of 2x mastermix, substitute
17 * 2 = 34 µL of water with [[6x DNA loading buffer]].

> [!WARNING]
>Not all loading buffers are PCR compatible. Do not use other loading buffers in the lab without verifying tha
>the buffer is compatible with PCR

# Using 6× Loading Buffer

A **6× loading buffer** must be diluted to **1× final concentration** in the DNA sample.

1 part 6× loading buffer + 5 parts DNA sample

The sample preparation depends on how much DNA we expect in the sample.
It is not advisable to load more than 10 µL

| 6× loading buffer (µL) | H2O | DNA sample | Total volume |                          |
| ---------------------- | --- | ---------- | ------------ | ------------------------ |
| 1                      | -   | 5          | 6            | Standard for PCR product |
| 1.5                    | -   | 8.5        | 10           | For a weak PCR product   |
| 1                      | 3   | 2          | 6            | Typical plasmid miniprep |

If you analyse a [[restriction digestion]], it is important to load an equal amount of undigested DNA as a reference.

For example, if you digested 2 µL plasmid DNA in a total of 10 µL and you want to analyze 5 µL on a gel, this sample effectively contains 1 µL of the original DNA.

If you have several, samples, spot the loading buffer on a piece of parafilm as shown below. Add water if needed
and then the DNA just before loading the gel. This saves a lot of time and plastic tubes.


![[GEL-1.png]]

# Typical Agarose Gel Percentages

| Agarose % | DNA size resolution |                          |
| --------- | ------------------- | ------------------------ |
| 0.7 %     | 0.8–10 kb           |                          |
| 1.0 %     | 0.5–7 kb            | We routinely use 1% gels |
| 1.5 %     | 0.2–3 kb            |                          |
| 2.0 %     | 0.1–2 kb            |                          |

Higher agarose concentrations resolve smaller fragments better.


<http://www.gelanalyzer.com/index.html>
<http://sourceforge.net/projects/pyelph/files/releases/>




- [[How many times can I reuse electrophoresis buffer?]]
- [[TAE]]
- [[fatval]]
- [[Turner]]
- [[Bachman]]
- [[Midori Green DNA loading buffer (LBx2wMidori)]]
- [[LiAc Borate]]
