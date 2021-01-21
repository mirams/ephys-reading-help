# Terminology for reading cardiac cell ephys lit

Goal is to make reading easy / possible.
It's not an encyclopedia.

## Currents

Below is a **deliberately incomplete and oversimplified** list of ionic currents in cardiac excitable cells, along with protein names, gene names (primarily the alpha subunits), some famous blockers, and unfortunate names still used in the literature.

| Current   | Protein(s) | Famous genes | Subunit genes              | Famous blockers         | Nicknames |
|-----------|------------|--------------|----------------------------|-------------------------|-----------|
| INa, INaL | Nav1.5     | SCN5A        | SCN1B, SCN2B, SCN3B, SCN4B | Tetrodotoxin (TTX), STX |           |
| ICaL      | Cav1.2     | CACNA1C      | CACNB2, CACNA2D1           |                         |           |
| ICaL      | Cav1.3     | CACNA1D      | CACNB2, CACNA2D1           | Nifedipine              |           |
| ICaT      | Cav3.2     | CACNA1H      |                            |                         |           |
| IKr       | Kv11.1     | KCNH2        | KCNE2                      | Dofetilide              | HERG      |
| IK1       | Kir2.1     | KCNJ2        |                            |                         |           |
| IKs       | Kv7.1      | KCNQ1, KCNE1 |                            |                         | LQT1      |
| Ito       | Kv4.3      | KCND3        |                            |                         |           |
| If        |            | HCN4         |                            |                         |           |
| IKur      | Kv1.5      | KCNA5        |                            |                         |           |

| Current     | Enzyme      | Famous genes | Subunit genes              | Famous blockers   |
|-------------|-------------|--------------|----------------------------|-------------------|
| INaK (Ip)   | Na/K-ATPAse |              |                            | Ouabain           |
| INaCa (NCX) |             |              |                            |                   |
|             | RyR         |              |                            |                   |
|             | SERCA       |              |                            |                   | 

#### Notes / Questions / TODO

- IClCa=Ito2, Ito=Ito1, IKur=IKp?
- Nav2.1 (SCN7A) also prevalent in heart?
- Gaborit Kv4.3 expr is surprising
- Other Kirs expressed in several places
- Kv1.7 (KCNA7) said to be similar to similar to Kv1.5 and important in atria

#### Why all these names? 

- The current is usually discovered long before the carrier (proteins/enzymes encoded by several genes).
- The gene products assemble in macromolecular complexes, which interact with other stuff in the cells. The current in the "Current" column is the current through these assemblies, present only in the native cell.
- To measure these, you need to get rid of other currents measured simultaneously, so you apply a blocker which you _hope_ is specific, but which you _suspect_ might not be, and so it is often "more correct" to say "we measured the dofetilide-sensitive current" rather than "we measured IKr". It also happens that currents are discovered through blockers, so the blocker is known before the current is named.
- In expression systems (CHO, HEK, Oocytes) you often express _only the alpha subunit_, so the channels lack all sorts of things they have in the real cells, and it can be more accurate to say "we measured a KCNH2 current" than "we measured IKr".
- Finally, a lot of genes had strange names until they became standardised. For example, "hERG" for "human Ether-a-go-go-Related Gene" because it is similar to a gene that made fruit fly legs twitch in early experiments. Some diseases have been classified by the genes suspected to underlie them, e.g. long QT syndrome got split into types according to various channel genes, where "LQT1" is the variant caused by IKs mutations. This then rubbed off onto the gene KCNQ1, so that some publications call it LQT1!

### Awesome references, per current

Awesome references for currents given below.
Bonus points if you can limit it to 1 ref per current.

| Current | Awesome ref                                                            |
| --------|------------------------------------------------------------------------|
| IKr     | [Vandenberg et al. (2012)](https://doi.org/10.1152/physrev.00036.2011) |
| ICaL    | [Striessnig et al. 2014](https://doi.org/10.1002/wmts.102)             |
|         | [Zamponi et al. 2015](https://doi.org/10.1124/pr.114.009654)           |
|         | [Hess 1988](https://doi.org/10.1139/y88-201)                           |
| INa     | [Grant 2001](https://doi.org/10.1016/S0002-9343(00)00714-2)            |
|         | [Chadda et al. 2017](https://doi.org/10.1007/s00424-017-1959-1)        |
| INaK    | [Glitsch 2001](https://doi.org/10.1152/physrev.2001.81.4.1791)         |

### More comprehensive current/channel/gene lists

- [Gaborit, Le Bouter et al., Nattel (2007) Regional and tissue specific transcript signatures of ion channel genes in the non‐diseased human heart](https://doi.org/10.1113/jphysiol.2006.126714)
- [EPFL Channelpedia](https://channelpedia.epfl.ch/)
- [IUPHAR/BPS List of channels](https://www.guidetopharmacology.org/GRAC/IonChannelListForward?class=VGIC)

## Nervous system

*Autonomic nervous system* (ANS) controls lots of organs (subconciously) including effects on the heart rate.

It's divided into **sympathetic** ("fight-or-flight"), **parasympathetic** ("rest-and-digest"), and enteric (your "gut brain" in popular science).

| Part of ANS     | Famous effect | Famous neurotransmitter             | Famous receptors      | Famous nerves   |
|-----------------|---------------|-------------------------------------|-----------------------|-----------------|
| Sympathetic     | Faster        | Epinephrine (Adrenaline)            | (Beta-) Adrenergic    |                 |
|                 |               | Experiments use Isoproterenol (iso) |                       |                 |
|                 |               | Norepinephrine (Noradrenaline)      |                       |                 |
|                 |               | Catecholamines                      |                       |                 |
| Parasympathetic | Slower        | Acetylcholine (ACh)                 | Muscarinic, Nicotinic | Vagus ("Vagal") |

## Annoying terminology

### Depolarisation

- When a membrane potential goes "up" from its resting potential value towards zero it "depolarises".
- When a membrane potential goes "down" from its resting potential value further from zero it "hyperpolarises".
- These terms are really useful when describing the resting potential, because a "higher resting potential" is ambiguous (bigger difference or higher value of V?).
- However, also used for membrane potential, where it gets annoying, with authors even calling a change from 10mV to 30mV a "depolarisation".
- (In 1902 the resting potential and action potential had been observed, but the membrane is much too small for light microscopy. Julius Bernstein proposed the existence of a membrane to explain the resting & action potential, and further hypothesised "membrane breakdown" as the explanation for depolarisation accompanied by changes to ion permeabilities. Kenneth Cole & collaborators performed early voltage-clamp experiments in the 30s and 40s and found that the membrane potential did not go to zero, but went to positive values, which they called "overshoot". This disproved the "membrane breakdown" idea, and maybe should have inspired some better terminology).

### Inotropic / Lusitropic

- "Positively inotropic" = increases strength of contraction / contractility
- "Negatively inotropic" = decreases strength of contraction / contractility
- "Positively lusitropic" = increases rate of relaxation
