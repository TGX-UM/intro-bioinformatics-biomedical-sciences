(db-p1-a5)=
# Assignment 5: Your version's compound in ChEBI and PubChem

*Time: 15 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

This assignment comes in three versions (A, B and C); see the version table on the practical page ({ref}`db-p1-versions`).

*Background: the [Reference guide](../guide/index.md) has one page per database.*

Pathways contain not only genes and proteins but also small molecules: hormones, metabolites, drugs. Chemical databases describe these. **ChEBI** (Chemical Entities of Biological Interest, at EMBL-EBI) is a curated dictionary of small molecules, with their structure and their biological *roles*. **PubChem** (at NCBI) is a very large collection that gathers information from hundreds of sources, including bioactivity, safety and literature. Use the compound and pathway of your version (see the table above).

:::{exercise} Question 1
:label: db-p1a5-q1
:nonumber:
Open the pathway of your version and click the compound. Which database does the pathway use to identify it, and what is the identifier?
:::

:::{solution} db-p1a5-q1
:class: dropdown
- **A — Estrogens (WP4194):** ChEBI, CHEBI:50114.
- **B — Creatine (WP5190):** ChEBI, CHEBI:16919.
- **C — Calcitriol (WP1531):** HMDB (Human Metabolome Database), HMDB0001903. Not every pathway uses ChEBI; you will need to translate this identifier in the next question.

```{figure} ../figures/2a-train-A-wp4194.png
:name: db-fig-2a-train-A-wp4194
:alt: Version A: WP4194, Estrogens ringed.

Version A: WP4194, Estrogens ringed. Figure from WikiPathways WP4194 (CC0).
```

```{figure} ../figures/2a-train-B-wp5190.png
:name: db-fig-2a-train-B-wp5190
:alt: Version B: WP5190, creatine ringed.

Version B: WP5190, creatine ringed. Figure from WikiPathways WP5190 (CC0).
```

```{figure} ../figures/2a-train-C-wp1531.png
:name: db-fig-2a-train-C-wp1531
:alt: Version C: WP1531, calcitriol ringed.

Version C: WP1531, calcitriol ringed. Figure from WikiPathways WP1531 (CC0).
```

*Checked 2026-10-23, WikiPathways.*
:::

:::{exercise} Question 2
:label: db-p1a5-q2
:nonumber:
Find your compound in ChEBI (<https://www.ebi.ac.uk/chebi/>). Version A: CHEBI:50114 does not describe one molecule; find out what it is, then look up **estradiol**. Version C: search ChEBI for **calcitriol**. Give the ChEBI name, identifier and molecular formula, and two of the roles ChEBI lists.
:::

:::{solution} db-p1a5-q2
:class: dropdown
- **A:** CHEBI:50114 is **estrogen**, a *role* that ChEBI defines as a hormone that stimulates or controls female sex characteristics by binding to oestrogen receptors. It has no structure of its own; many molecules have this role (estrone, estradiol, estriol and synthetic ones). The pathway box "Estrogens" stands for the whole group. The main human estrogen is **17β-estradiol**, CHEBI:16469, C₁₈H₂₄O₂. Roles include *estrogen*, *human metabolite* and *geroprotector*.
- **B:** **creatine**, CHEBI:16919, C₄H₉N₃O₂, defined as a glycine derivative. Roles include *human metabolite*, *nutraceutical*, *neuroprotective agent* and *geroprotector*.
- **C:** **calcitriol**, CHEBI:17823, C₂₇H₄₄O₃, the active form of vitamin D₃. Roles include *hormone*, *bone density conservation agent* and *human metabolite*.

```{figure} ../figures/2a-train-A-chebi.png
:name: db-fig-2a-train-A-chebi
:alt: Version A: ChEBI CHEBI:16469, estradiol.

Version A: ChEBI CHEBI:16469, estradiol. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

```{figure} ../figures/2a-train-B-chebi.png
:name: db-fig-2a-train-B-chebi
:alt: Version B: ChEBI CHEBI:16919, creatine.

Version B: ChEBI CHEBI:16919, creatine. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

```{figure} ../figures/2a-train-C-chebi.png
:name: db-fig-2a-train-C-chebi
:alt: Version C: ChEBI CHEBI:17823, calcitriol.

Version C: ChEBI CHEBI:17823, calcitriol. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, ChEBI.*
:::

:::{exercise} Question 3
:label: db-p1a5-q3
:nonumber:
Look up the same compound in PubChem. What is its PubChem CID? Give one kind of information that PubChem shows and ChEBI does not.
:::

:::{solution} db-p1a5-q3
:class: dropdown
- **A:** estradiol, CID 5757.
- **B:** creatine, CID 586.
- **C:** calcitriol, CID 5280453.

PubChem gathers far more, from many sources. Examples: drug and medication information, pharmacology, safety and hazards (GHS classification), toxicity, bioassay results, patents, vendors and literature counts. ChEBI is smaller and curated, and focuses on what the molecule *is* and which roles it has. The two complement each other: ChEBI for a precise, curated identity; PubChem for everything that has been reported about the compound.

*Checked 2026-10-23, PubChem.*
:::

:::{exercise} Question 4
:label: db-p1a5-q4
:nonumber:
Read the ChEBI definition and roles of your compound (version A: of estradiol). How does it connect to the theme of your version (see the version table)?
:::

:::{solution} db-p1a5-q4
:class: dropdown
- **A (hormones and puberty):** estradiol is the main estrogen. In puberty it stimulates the growth spurt (via GH and IGF1, as in the pathway) and later closes the growth plates. Its role as *geroprotector* links to ageing.
- **B (muscle):** creatine stores energy in muscle as phosphocreatine (also in the pathway), which regenerates ATP during short bursts of contraction. That is why it is used as a supplement (*nutraceutical*). Its breakdown product creatinine (CHEBI:16737) is used clinically as a marker of kidney function and muscle mass.
- **C (bone):** calcitriol is made in the kidney from calcidiol and increases calcium uptake from the gut. Calcium is needed for bone mineralisation, hence the role *bone density conservation agent*.
:::
