(db-p2-a2)=
# Assignment 2: The APC protein in UniProt

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

Now we turn to the UniProt database, to find more information about the function and structure of the protein encoded by the gene from the second assignment. First, go to the UniProt page of the human protein of APC (<https://www.uniprot.org/uniprotkb/P25054/entry>).

:::{exercise} Question 1
:label: db-p2a2-q1
:nonumber:
What is the UniProt name and identifier of the human APC protein, and what is the entry’s review status?
:::

:::{solution} db-p2a2-q1
:class: dropdown
The human APC protein is listed as *Adenomatous polyposis coli protein*, with UniProt identifier P25054. The entry is reviewed (Swiss-Prot), meaning it has undergone expert curation.

```{figure} ../figures/2b-prep-uni-names.png
:name: db-fig-2b-prep-uni-names
:alt: UniProt P25054, entry header.

UniProt P25054, entry header. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

The page starts off with a concise description of the function of the protein, supported by references.

:::{exercise} Question 2
:label: db-p2a2-q2
:nonumber:
How many references are supporting the function description, and which one is most recent?
:::

:::{solution} db-p2a2-q2
:class: dropdown
UniProt cites six publications supporting APC’s functional description. The most recent reference is from 2010 (Zaoui et al.).

```{figure} ../figures/2b-prep-uni-function.png
:name: db-fig-2b-prep-uni-function
:alt: UniProt P25054, Function.

UniProt P25054, Function. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Further on, in the “Miscellaneous” paragraph at the bottom of the *Function* section, some generic information on the types and positions of the mutations is given.

:::{exercise} Question 3
:label: db-p2a2-q3
:nonumber:
Does the information on mutations given by UniProt correspond to what you found for rs137854573 in dbSNP and ClinVar (assignment 2, question 8)?
:::

:::{solution} db-p2a2-q3
:class: dropdown
Yes. Both link APC mutations to familial adenomatous polyposis (FAP) and colorectal cancer, and UniProt notes that most disease mutations truncate the protein, as the pathogenic C→T allele (R554\*) does. UniProt describes the effects at the protein level, while dbSNP and ClinVar describe single variants and their clinical classification, so the details differ but the overall picture agrees.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Further on, information on the GO annotations for the protein is given, based on Molecular function and Biological process (cellular component are listed in a graphical overview further down on the page). Click the small “i” next to “GO annotations” for an explanation on what GO (Gene Ontology) is.

:::{exercise} Question 4
:label: db-p2a2-q4
:nonumber:
In the overview of terms in the side-scrolling window, click the “All Biological Process” box (if a “Slimming set” drop-down is shown above the ribbon, leave it at its default) to filter the table for processes in which APC is involved. What is the evidence type and PubMed ID for the GO Biological Process annotation “DNA damage response”?
:::

:::{solution} db-p2a2-q4
:class: dropdown
The annotation is supported by experimental evidence (IDA: Inferred from Direct Assay). The associated PubMed ID is 14728717.

```{figure} ../figures/2b-prep-uni-go.png
:name: db-fig-2b-prep-uni-go
:alt: UniProt P25054, GO annotations.

UniProt P25054, GO annotations. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 5
:label: db-p2a2-q5
:nonumber:
Moving to the section “Subcellular Location”: Which general subcellular locations are given for this protein by “UniProt annotation”? How many references are given (in total), for these annotations?
:::

:::{solution} db-p2a2-q5
:class: dropdown
UniProt annotation gives: cell junction (adherens junction), cytoskeleton, lamellipodium, ruffle membrane, cytoplasm and cell membrane.

Count the publications shown next to these locations: 1 + 2 + 1 + 1 + 1 + 3 = 9 (12 if you also count the 3 under the Note), from 5 distinct papers. The number depends on whether you count each citation or each distinct paper: the same publication can support several locations. Comparing them by hand is possible by opening each publication box; with a script it can be done automatically, which is outside this practical.

```{figure} ../figures/2b-prep-uni-location.png
:name: db-fig-2b-prep-uni-location
:alt: UniProt P25054, Subcellular Location.

UniProt P25054, Subcellular Location. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-28, UniProt release 2026_03.*
:::

:::{exercise} Question 6
:label: db-p2a2-q6
:nonumber:
Which of these UniProt annotations overlap with the subcellular locations given for this protein by the GO cellular-component annotation (Hint: click the second tab, labelled “GO Annotation”, next to the cellular drawing)? Which major organelle is annotated as a cellular location with GO, but is missing with UniProt?
:::

:::{solution} db-p2a2-q6
:class: dropdown
Both list adherens junction, ruffle membrane, cytoplasm, (plasma) membrane and lamellipodium. GO adds the **nucleus** (and nucleoplasm), the major organelle missing from the UniProt annotation, plus more specific places and complexes: cytosol, centrosome, kinetochore, tight junctions, the β-catenin destruction complex and the Wnt signalosome. UniProt's "cytoskeleton" appears in GO only as a specific part (the centrosome).

*Checked 2026-10-28, UniProt release 2026_03 (GO cellular component annotations).*
:::

:::{exercise} Question 7
:label: db-p2a2-q7
:nonumber:
UniProt and GO list slightly different subcellular locations for APC. What might explain these differences?
:::

:::{solution} db-p2a2-q7
:class: dropdown
They use different evidence sources and curation pipelines. UniProt relies on curated literature; GO integrates many databases and inference methods. This can lead to additional or missing terms in one database.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Scrolling further down the page (in the section “Disease & Variants”), we find an overview of involvement of mutations in the protein in human disease. For the next question, we will only focus on the “Familial adenomatous polyposis 1 (FAP1)” disease.

:::{exercise} Question 8
:label: db-p2a2-q8
:nonumber:
What is the OMIM identifier for FAP1?
:::

:::{solution} db-p2a2-q8
:class: dropdown
175100

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 9
:label: db-p2a2-q9
:nonumber:
How many APC variants associated with FAP1 are listed in UniProt, and how many have a dbSNP ID? Use the “Natural variants in FAP1” table inside the Disease & Variants section — not the separate Variant viewer tab, which lists far more.
:::

:::{solution} db-p2a2-q9
:class: dropdown
13 variants, of which 6 have a dbSNP ID.

```{figure} ../figures/2b-prep-uni-disease.png
:name: db-fig-2b-prep-uni-disease
:alt: UniProt P25054, Disease & Variants.

UniProt P25054, Disease & Variants. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

After the disease-associated mutations, a section is presented on processing of the protein (*e.g.* cleaving, amino acid modifications, aka Post Translational Modifications or PTMs).

:::{exercise} Question 10
:label: db-p2a2-q10
:nonumber:
Which is the most common modification present for this protein? Why might this modification be an important modification for a protein involved in cell cycle control and signal transduction?
:::

:::{solution} db-p2a2-q10
:class: dropdown
The most common modification is phosphorylation of serine (phosphoserine). In APC, serine phosphorylation helps regulate how the protein interacts with partners in the Wnt/β-catenin signaling pathway and supports proper control of cell proliferation. Because APC acts as a tumor suppressor, phosphorylation is important for adjusting its activity within cell-cycle and signaling processes.

```{figure} ../figures/2b-prep-uni-ptm.png
:name: db-fig-2b-prep-uni-ptm
:alt: UniProt P25054, PTM/Processing.

UniProt P25054, PTM/Processing. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 11
:label: db-p2a2-q11
:nonumber:
What is the biological function of this type of modification in general (look up some details for this question outside of UniProt)?
:::

:::{solution} db-p2a2-q11
:class: dropdown
Phosphorylation is a reversible post-translational modification in which a phosphate group is added to serine, threonine, or tyrosine residues. It functions as a molecular switch that can rapidly change a protein’s activity, stability, structure, cellular location, or interaction partners. This makes phosphorylation a central mechanism in regulating key cellular processes such as signal transduction, cell growth, and the cell cycle.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Also, scrolling further down, information on interaction partners of the protein is given. Use the Binary interactions figure for the following questions. If it looks crowded, click “Expand table” below the table and compare the “Number of experiments” column.

:::{exercise} Question 12
:label: db-p2a2-q12
:nonumber:
Which protein shows the strongest interaction support with APC according to UniProt, and how many experimental observations support this interaction? How many experiments have been performed to establish this interaction (click on the dot to obtain more information)?
:::

:::{solution} db-p2a2-q12
:class: dropdown
Some dots are clearly darker in colour than others; these do not actually indicate strength of the interaction, but the colors are based on the number of experiments that support the interaction. The interactions with most support include interactions between APC and CTNB1_HUMAN, AXIN1_HUMAN, and DLG1_HUMAN (compare only the first column with one another, or look into the table below the figure). We will now focus on CTNB1_HUMAN; clicking on the dot reveals there are 22 experiments which confirmed this interaction.

```{figure} ../figures/2b-prep-uni-interaction.png
:name: db-fig-2b-prep-uni-interaction
:alt: UniProt P25054, Interaction.

UniProt P25054, Interaction. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-28, UniProt release 2026_03.*
:::

Finally, we will have a look at the structural information given in UniProt.

:::{exercise} Question 13
:label: db-p2a2-q13
:nonumber:
In general, which secondary protein structural elements exist?
:::

:::{solution} db-p2a2-q13
:class: dropdown
Helixes (alpha), turns, beta sheets. (Random coils and “other” structures are also known, but less common).

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Switch to the “Feature viewer” tab at the top of the page. UniProt no longer groups helices, strands and turns under a “Structural features” heading, so use the **PDBe 3D structure coverage** and **AlphaFold** tracks to see which parts of the protein are structured, and look at those parts in the 3D viewer of the *Structure* section on the entry page (helices are drawn as spirals, strands as arrows).

:::{exercise} Question 14
:label: db-p2a2-q14
:nonumber:
Which secondary structural element is most common for the APC protein, and where in the protein does it mostly occur?
:::

:::{solution} db-p2a2-q14
:class: dropdown
α-helix, by a wide margin, and concentrated in the N-terminal third of the protein. UniProt annotates 41 helices against 4 β-strands and 3 turns; about thirty of those helices fall between residues 328 and 742, which is the armadillo (ARM) repeat region, with a further cluster in the N-terminal oligomerisation region. That is also the part of APC for which experimental structures exist — which is exactly why it is the part with secondary structure annotated.

⚠️ **Note the interface changed.** UniProt removed the “Structural features” grouping from the Feature viewer in late 2025, so a previous year's instruction to open it no longer works. Read the structure from the *PDBe 3D structure coverage* and *AlphaFold* tracks and from the 3D viewer in the *Structure* section instead.

⚠️ **Release-volatile** — the helix count was 36 in 2025.

```{figure} ../figures/2b-prep-uni-structure.png
:name: db-fig-2b-prep-uni-structure
:alt: UniProt P25054, Structure.

UniProt P25054, Structure. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::
