---
publish: true
---

## Harnessing Microbial Cell Factories for Essential Fatty Acid Production

Fatty acids are fundamental building blocks of life, with roles in energy storage, membrane architecture, and cellular signalling. Among these, long-chain polyunsaturated fatty acids (LC-PUFAs) are particularly important in human biology, contributing to the development and maintenance of the brain, retina, and immune system throughout the lifespan. These fatty acids are commercially important nutraceuticals, routinely supplemented in infant formula, clinical nutrition, and dietary supplements. Their market has grown steadily, driven by evidence linking dietary PUFA intake to reduced incidence of neurological, metabolic, and inflammatory disease.

| Acronym | Name                                                                               | Chain | Series | Double bonds         | Description                                                                                                                                                                                                                  |
| ------- | ---------------------------------------------------------------------------------- | ----- | ------ | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GLA     | [γ-Linolenic acid](https://en.wikipedia.org/wiki/Gamma-Linolenic_acid)             | C18:3 | ω-6    | 3 (Δ6,9,12)          | Precursor to **ARA** via DGLA. Naturally produced by oleaginous fungi (*Mortierella*, *Mucor*); an early benchmark target in microbial PUFA engineering.                                                                     |
| SDA     | [Stearidonic acid](https://en.wikipedia.org/wiki/Stearidonic_acid)                 | C18:4 | ω-3    | 4 (Δ6,9,12,15)       | The ω-3 analogue of GLA; a more efficient dietary precursor to EPA than α-linolenic acid. Found in *Echium* and some microalgae. An attractive shorter-chain EPA precursor target for yeast engineering.                     |
| ARA     | [Arachidonic acid](https://en.wikipedia.org/wiki/Arachidonic_acid)                 | C20:4 | ω-6    | 4 (Δ5,8,11,14)       | Structural component of neuronal phospholipids; precursor to eicosanoids (prostaglandins, leukotrienes) involved in inflammatory signalling. Supplied in infant formula; produced industrially in *Mortierella alpina*.      |
| EPA     | [Eicosapentaenoic acid](https://en.wikipedia.org/wiki/Eicosapentaenoic_acid)       | C20:5 | ω-3    | 5 (Δ5,8,11,14,17)    | Precursor to resolvins and protectins; reduces neuroinflammation. Associated with reduced risk of depression and cardiovascular disease.                                                                                     |
| DPA     | [Docosapentaenoic acid (n-3)](https://en.wikipedia.org/wiki/Docosapentaenoic_acid) | C22:5 | ω-3    | 5 (Δ7,10,13,16,19)   | Elongation product of EPA and the direct precursor to DHA in the Sprecher pathway. Accumulates when Δ4-desaturase activity is limiting; relevant as an intermediate and potential co-product in DHA-producing yeast strains. |
| DHA     | [Docosahexaenoic acid](https://en.wikipedia.org/wiki/Docosahexaenoic_acid)         | C22:6 | ω-3    | 6 (Δ4,7,10,13,16,19) | The most abundant ω-3 in brain and retina; important for synaptic plasticity, membrane fluidity, and visual acuity. Synthesised from EPA via the Sprecher pathway. Mandatory in infant formula in many countries.            |

**The supply problem.** The dominant commercial sources today are fish oil from pelagic fisheries and krill oil. Both present sustainability challenges. Many commercially targeted fish stocks are under pressure from overexploitation, while krill occupy the base of the ocean food web and their harvest carries ecosystem risks.

![[2026-03-31.png]]

Critically, neither fish nor krill synthesize LC-PUFAs themselves, they bio-accumulate them from the phytoplankton they consume. Phytoplankton produce PUFAs as an adaptive response to cold temperatures, where highly unsaturated membranes maintain fluidity. Climate change is disrupting this: rising ocean temperatures suppress PUFA biosynthesis in phytoplankton and shift community composition, with documented reductions in EPA and DHA concentrations in marine biomass. The marine source of our PUFA supply is therefore simultaneously being over-harvested and diminished by warming seas.

**Microbial biosynthesis as an alternative.** Oleaginous microorganisms, yeasts, microalgae, and filamentous fungi can replicate the biosynthetic capacity of phytoplankton in a controllable fermentation context. Among candidate hosts, _Saccharomyces cerevisiae_ is genetically accessible, grows rapidly on inexpensive carbon sources, is GRAS-classified, and benefits from well-established industrial fermentation infrastructure. Its lipid metabolism is well characterised, providing a rational starting point for engineering.

![[2026-03-31-2.png]]

**FAS system II**

In most eukaryotes, LC-PUFA biosynthesis proceeds via sequential aerobic desaturation and elongation acting on acyl-CoA or acyl-lipid substrates. _S. cerevisiae_ lacks this capacity almost entirely, retaining only the single Δ9-desaturase Ole1p. Introducing unsaturated fatty acid biosynthesis therefore requires a different approach.

One strategy is to express a complete, self-contained system based on the bacterial type II fatty acid synthase (FASII). Unlike the eukaryotic type I FAS, a large multifunctional complex that releases its product only upon chain termination, FASII operates through discrete, dissociable enzymes that carry acyl intermediates on a small acyl carrier protein (ACP).

This architecture is compatible with acyl-ACP desaturases: soluble enzymes that introduce double bonds directly onto the acyl chain while it remains ACP-bound, before release from the synthase. Unsaturation is therefore built in during elongation rather than added post-synthetically. This is a meaningful mechanistic advantage, because once a fatty acid is released as acyl-CoA or incorporated into a lipid, enzymes such as elongases, acyltransferases and degradative enzymes all compete for the same substrate. Acting at the acyl-ACP stage sidesteps much of this competition and may allow greater control over the final product profile.

![[2026-03-31-4.png]]
