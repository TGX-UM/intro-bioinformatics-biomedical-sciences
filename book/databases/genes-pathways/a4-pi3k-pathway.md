(db-p1-a4)=
# Assignment 4: Another biological context of IGF-1 from WikiPathways

*Time: 20 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

Look up the human "Focal adhesion: PI3K-Akt-mTOR-signaling pathway" in WikiPathways (<https://www.wikipathways.org/pathways/WP3932>). This database shows you interactive drawings of pathway diagrams, which help to understand the biological context of genes, proteins and metabolites. The current pathway is extensive, but the focus is in particular on IGF-1 and the PI3K-Akt-mTOR pathway that regulate cell growth and protein synthesis.

:::{exercise} Question 1
:label: db-p1a4-q1
:nonumber:
To which category of (extracellular) signalling molecules does IGF1 belong, according to the pathway? (Hint: open <https://pathway-viewer.toolforge.org/embed/WP3932?lightgreen=IGF1&red=IGF1R>; the viewer highlights IGF1 in green and IGF1R in red for you. Your browser's find-in-page will also locate the labels, but the diagram is wide and it will not scroll to them.)
:::

:::{solution} db-p1a4-q1
:class: dropdown
IGF1 belongs to the **growth factors**, a class of extracellular proteins that stimulate cell proliferation, survival and growth by binding to specific receptors. IGF1 binds the IGF1 receptor (IGF1R), which belongs to the group of receptor tyrosine kinases (RTKs). If you chose version C: FGFR3, your gene in assignment 3, sits in the same RTK box.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 2
:label: db-p1a4-q2
:nonumber:
What are the Ensembl identifier and HGNC symbol of IGF1R? Hint: click the pathway diagram to open the interactive viewer, then click the IGF1R box: it takes you to the gene page in a new tab. Alternatively, find IGF1R in the Participants table on the pathway page.

Ensembl:

HGNC symbol:
:::

:::{solution} db-p1a4-q2
:class: dropdown
Ensembl: ENSG00000140443

HGNC symbol: IGF1R (full name *insulin like growth factor 1 receptor*, HGNC:5465)

```{figure} ../figures/2a-train-wp3932.png
:name: db-fig-2a-train-wp3932
:alt: WikiPathways WP3932, IGF1 and IGF1R ringed.

WikiPathways WP3932, IGF1 and IGF1R ringed. Figure from WikiPathways WP3932 (CC0).
```

*Checked 2026-10-23, Ensembl gene ENSG00000140443.15.*
:::

:::{exercise} Question 3
:label: db-p1a4-q3
:nonumber:
If a mutation reduces IGF1R activity by 50%, which part of the PI3K–Akt–mTOR pathway would be affected first, and what biological consequences could this have?
:::

:::{solution} db-p1a4-q3
:class: dropdown
The first affected step is the activation of PI3K, because PI3K is recruited and activated by IGF1R via adaptor proteins (e.g. IRS1/2). With reduced PI3K activation:

- less PIP3 is formed;
- downstream effectors such as Akt (PKB) are less activated;
- mTOR receives reduced stimulation;
- protein synthesis and cell growth decrease.

Biological consequences may include impaired growth and reduced muscle protein synthesis, a delayed pubertal growth spurt, reduced cell-survival signals, and growth defects similar to IGF1-deficiency phenotypes.
:::

:::{exercise} Question 4
:label: db-p1a4-q4
:nonumber:
Molecules that belong to this category activate the receptor tyrosine kinases (RTKs), which is indicated by the label above the group of proteins. These (indirectly) stimulate PI3K (class IA and II). Which other types of extracellular molecules, consisting of protein(s) (black boxes), have an effect on PI3K?
:::

:::{solution} db-p1a4-q4
:class: dropdown
ECM (extracellular matrix) proteins and cytokines. The two vertical lines indicate the cell membrane; the molecules on the left side are extracellular.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 5
:label: db-p1a4-q5
:nonumber:
Which other compound(s)/metabolites (blue boxes) can have an effect on PI3K activity?
:::

:::{solution} db-p1a4-q5
:class: dropdown
NO (nitric oxide) and insulin. Although shown as a metabolite in the pathway diagram, insulin is a peptide hormone, and biologically similar to IGF1 in receptor signalling.

```{figure} ../figures/2a-train-wp3932-compounds.png
:name: db-fig-2a-train-wp3932-compounds
:alt: WikiPathways WP3932, NO and insulin ringed.

WikiPathways WP3932, NO and insulin ringed. Figure from WikiPathways WP3932 (CC0).
```

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 6
:label: db-p1a4-q6
:nonumber:
Click each of these two compounds in the pathway viewer. Which **ChEBI** identifier does the pathway give for each? Then search PubChem (<https://pubchem.ncbi.nlm.nih.gov/>) for each compound by name and note its **PubChem CID** (compound identifier).

| | Compound 1 | Compound 2 |
|---|---|---|
| Label | | |
| ChEBI ID (from the pathway) | | |
| PubChem CID | | |
:::

:::{solution} db-p1a4-q6
:class: dropdown
| | Compound 1 | Compound 2 |
|---|---|---|
| Label | NO | Insulin |
| ChEBI ID (from the pathway) | CHEBI:29120 | CHEBI:5931 |
| PubChem CID | 145068 when you search "nitric oxide"; but see question 7 | 118984375 ("Insulin Human") |

Insulin gives several PubChem hits (human insulin, insulin from other species), because PubChem stores each distinct chemical structure as its own compound. Look at the name and formula to pick the right one.

*Checked 2026-10-23, WikiPathways, ChEBI and PubChem.*
:::

:::{exercise} Question 7
:label: db-p1a4-q7
:nonumber:
Open the ChEBI entry for the `NO` identifier that the pathway gives (<https://www.ebi.ac.uk/chebi/CHEBI:29120>). What is the ChEBI name of this entity, what is its charge, and which biological **roles** does ChEBI list for it? Now open CHEBI:16480 (<https://www.ebi.ac.uk/chebi/CHEBI:16480>). What is this, and which roles does it have? Which of the two is the signalling molecule that acts in this pathway, and what does that tell you about taking an identifier from a pathway on trust?
:::

:::{solution} db-p1a4-q7
:class: dropdown
CHEBI:29120 is **oxidonitrogen(1+)**, the nitrosonium cation NO⁺, with charge +1. ChEBI lists **no biological roles** for it: it is classified only as a nitrogen oxide and a monovalent inorganic cation.

CHEBI:16480 is **nitric oxide**, the neutral free radical (charge 0), with roles including *signalling molecule*, *vasodilator agent*, *neurotransmitter* and *human metabolite*.

The signalling molecule in biology is the nitric-oxide radical, CHEBI:16480, so the pathway's annotation points at a different chemical entity than the one the diagram means. Pathway diagrams are curated by people, and mistakes like this happen. Check that an identifier really describes what the label says before you use it. And since WikiPathways is a community resource, anyone, including you, can report or correct it.

```{figure} ../figures/2a-train-chebi-29120.png
:name: db-fig-2a-train-chebi-29120
:alt: ChEBI CHEBI:29120, the identifier the pathway uses.

ChEBI CHEBI:29120, the identifier the pathway uses. Screenshot of ChEBI, 2026-10-24 (CC BY 4.0).
```

```{figure} ../figures/2a-train-chebi-16480-roles.png
:name: db-fig-2a-train-chebi-16480-roles
:alt: ChEBI CHEBI:16480, nitric oxide radical: roles.

ChEBI CHEBI:16480, nitric oxide radical: roles. Screenshot of ChEBI, 2026-10-24 (CC BY 4.0).
```

*Checked 2026-10-23, ChEBI.*
:::

:::{exercise} Question 8
:label: db-p1a4-q8
:nonumber:
Take a look at mTOR, at the right side of the pathway. mTOR can stimulate cell growth and protein synthesis in multiple ways. In your own words, describe how mTOR stimulates cell growth and protein synthesis. What is the meaning of the different types of arrows/connections that you see in this area?
:::

:::{solution} db-p1a4-q8
:class: dropdown
Path 1: mTOR phosphorylates the ribosomal protein S6 kinases, which activate ribosomal protein S6 and EIF4B, leading to cell growth and protein synthesis.

Path 2: mTOR phosphorylates EIF4EBP1, thereby inhibiting it and releasing the EIF4E proteins, leading to cell growth and protein synthesis (inhibition of an inhibitor).

Interactions with normal arrowheads generally indicate a positive interaction: stimulation or activation. Interactions with a T-bar at their end indicate inhibition.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::
