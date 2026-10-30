(db-session-2a)=
# Practical 2A: computer session

*Time: about 2 hours. Do the [2A preparation](prep-2a.md) first.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

In the 2A preparation you used a disease database (OMIM), a pathway database (WikiPathways)
and a genomic database (Ensembl). In this session you explore another pathway (WikiPathways),
look up compounds in two chemical databases (ChEBI and PubChem), and continue with another
genomic database (NCBI Gene).

You will use the databases to study growth signalling. IGF-1 plays a critical role in many
developmental and growth processes. In the second half of this session you choose one of three
growth-related genes: IGF1 itself, or one of two genes from the bone and muscle cases.

*Background: the [Reference guide](guide/index.md) has one page per database.*


- In the preparation you studied the role of IGF-1 in the pubertal growth spurt with WikiPathways, and its involvement in disease and its gene structure with OMIM and Ensembl. IGF-1 also plays a central role in muscle and bone growth and in stimulating protein synthesis.

- Assignment 1 is the same for everyone: IGF-1 in the PI3K-Akt-mTOR signalling pathway.

- Assignments 2 and 3 come in **three versions**, each tied to a tutorial case. Choose one version and work through it. If you have time left, or later to practise, do one of the other versions as well. At the end, compare your results with a classmate who chose a different version.

| | **Version A** | **Version B** | **Version C** |
|---|---|---|---|
| **Tutorial case** | 5: Hormones, growth and sexual development | 4: Cardiac and skeletal muscle | 3: Growing patterns: bone |
| **Compound (assignment 2)** | Estrogens, in [WP4194](https://www.wikipathways.org/pathways/WP4194.html) Hormonal control of pubertal growth spurt | Creatine, in [WP5190](https://www.wikipathways.org/pathways/WP5190.html) Creatine pathway | Calcitriol, in [WP1531](https://www.wikipathways.org/pathways/WP1531.html) Vitamin D metabolism |
| **Gene (assignment 3)** | IGF1, <https://www.ncbi.nlm.nih.gov/gene/3479> | MSTN, <https://www.ncbi.nlm.nih.gov/gene/2660> | FGFR3, <https://www.ncbi.nlm.nih.gov/gene/2261> |

## Assignment 1: Another biological context of IGF-1 from WikiPathways

*Time: 20 min.*

Look up the human "Focal adhesion: PI3K-Akt-mTOR-signaling pathway" in WikiPathways (<https://www.wikipathways.org/pathways/WP3932>). This database shows you interactive drawings of pathway diagrams, which help to understand the biological context of genes, proteins and metabolites. The current pathway is extensive, but the focus is in particular on IGF-1 and the PI3K-Akt-mTOR pathway that regulate cell growth and protein synthesis.

:::{exercise} Question 1
:label: db-s2a-a1-q1
:nonumber:
To which category of (extracellular) signalling molecules does IGF1 belong, according to the pathway? (Hint: open <https://pathway-viewer.toolforge.org/embed/WP3932?lightgreen=IGF1&red=IGF1R>; the viewer highlights IGF1 in green and IGF1R in red for you. Your browser's find-in-page will also locate the labels, but the diagram is wide and it will not scroll to them.)
:::

:::{solution} db-s2a-a1-q1
:class: dropdown
IGF1 belongs to the **growth factors**, a class of extracellular proteins that stimulate cell proliferation, survival and growth by binding to specific receptors. IGF1 binds the IGF1 receptor (IGF1R), which belongs to the group of receptor tyrosine kinases (RTKs). If you chose version C: FGFR3, your gene in assignment 3, sits in the same RTK box.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 2
:label: db-s2a-a1-q2
:nonumber:
What are the Ensembl identifier and HGNC symbol of IGF1R? Hint: click the pathway diagram to open the interactive viewer, then click the IGF1R box: it takes you to the gene page in a new tab. Alternatively, find IGF1R in the Participants table on the pathway page.

Ensembl:

HGNC symbol:
:::

:::{solution} db-s2a-a1-q2
:class: dropdown
Ensembl: ENSG00000140443

HGNC symbol: IGF1R (full name *insulin like growth factor 1 receptor*, HGNC:5465)

```{figure} figures/2a-train-wp3932.png
:name: db-fig-2a-train-wp3932
:alt: WikiPathways WP3932, IGF1 and IGF1R ringed.

WikiPathways WP3932, IGF1 and IGF1R ringed. Figure from WikiPathways WP3932 (CC0).
```

*Checked 2026-10-23, Ensembl gene ENSG00000140443.15.*
:::

:::{exercise} Question 3
:label: db-s2a-a1-q3
:nonumber:
If a mutation reduces IGF1R activity by 50%, which part of the PI3K–Akt–mTOR pathway would be affected first, and what biological consequences could this have?
:::

:::{solution} db-s2a-a1-q3
:class: dropdown
The first affected step is the activation of PI3K, because PI3K is recruited and activated by IGF1R via adaptor proteins (e.g. IRS1/2). With reduced PI3K activation:

- less PIP3 is formed;
- downstream effectors such as Akt (PKB) are less activated;
- mTOR receives reduced stimulation;
- protein synthesis and cell growth decrease.

Biological consequences may include impaired growth and reduced muscle protein synthesis, a delayed pubertal growth spurt, reduced cell-survival signals, and growth defects similar to IGF1-deficiency phenotypes.
:::

:::{exercise} Question 4
:label: db-s2a-a1-q4
:nonumber:
Molecules that belong to this category activate the receptor tyrosine kinases (RTKs), which is indicated by the label above the group of proteins. These (indirectly) stimulate PI3K (class IA and II). Which other types of extracellular molecules, consisting of protein(s) (black boxes), have an effect on PI3K?
:::

:::{solution} db-s2a-a1-q4
:class: dropdown
ECM (extracellular matrix) proteins and cytokines. The two vertical lines indicate the cell membrane; the molecules on the left side are extracellular.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 5
:label: db-s2a-a1-q5
:nonumber:
Which other compound(s)/metabolites (blue boxes) can have an effect on PI3K activity?
:::

:::{solution} db-s2a-a1-q5
:class: dropdown
NO (nitric oxide) and insulin. Although shown as a metabolite in the pathway diagram, insulin is a peptide hormone, and biologically similar to IGF1 in receptor signalling.

```{figure} figures/2a-train-wp3932-compounds.png
:name: db-fig-2a-train-wp3932-compounds
:alt: WikiPathways WP3932, NO and insulin ringed.

WikiPathways WP3932, NO and insulin ringed. Figure from WikiPathways WP3932 (CC0).
```

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

:::{exercise} Question 6
:label: db-s2a-a1-q6
:nonumber:
Click each of these two compounds in the pathway viewer. Which **ChEBI** identifier does the pathway give for each? Then search PubChem (<https://pubchem.ncbi.nlm.nih.gov/>) for each compound by name and note its **PubChem CID** (compound identifier).

| | Compound 1 | Compound 2 |
|---|---|---|
| Label | | |
| ChEBI ID (from the pathway) | | |
| PubChem CID | | |
:::

:::{solution} db-s2a-a1-q6
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
:label: db-s2a-a1-q7
:nonumber:
Open the ChEBI entry for the `NO` identifier that the pathway gives (<https://www.ebi.ac.uk/chebi/CHEBI:29120>). What is the ChEBI name of this entity, what is its charge, and which biological **roles** does ChEBI list for it? Now open CHEBI:16480 (<https://www.ebi.ac.uk/chebi/CHEBI:16480>). What is this, and which roles does it have? Which of the two is the signalling molecule that acts in this pathway, and what does that tell you about taking an identifier from a pathway on trust?
:::

:::{solution} db-s2a-a1-q7
:class: dropdown
CHEBI:29120 is **oxidonitrogen(1+)**, the nitrosonium cation NO⁺, with charge +1. ChEBI lists **no biological roles** for it: it is classified only as a nitrogen oxide and a monovalent inorganic cation.

CHEBI:16480 is **nitric oxide**, the neutral free radical (charge 0), with roles including *signalling molecule*, *vasodilator agent*, *neurotransmitter* and *human metabolite*.

The signalling molecule in biology is the nitric-oxide radical, CHEBI:16480, so the pathway's annotation points at a different chemical entity than the one the diagram means. Pathway diagrams are curated by people, and mistakes like this happen. Check that an identifier really describes what the label says before you use it. And since WikiPathways is a community resource, anyone, including you, can report or correct it.

```{figure} figures/2a-train-chebi-29120.png
:name: db-fig-2a-train-chebi-29120
:alt: ChEBI CHEBI:29120, the identifier the pathway uses.

ChEBI CHEBI:29120, the identifier the pathway uses. Screenshot of ChEBI, 2026-10-24 (CC BY 4.0).
```

```{figure} figures/2a-train-chebi-16480-roles.png
:name: db-fig-2a-train-chebi-16480-roles
:alt: ChEBI CHEBI:16480, nitric oxide radical: roles.

ChEBI CHEBI:16480, nitric oxide radical: roles. Screenshot of ChEBI, 2026-10-24 (CC BY 4.0).
```

*Checked 2026-10-23, ChEBI.*
:::

:::{exercise} Question 8
:label: db-s2a-a1-q8
:nonumber:
Take a look at mTOR, at the right side of the pathway. mTOR can stimulate cell growth and protein synthesis in multiple ways. In your own words, describe how mTOR stimulates cell growth and protein synthesis. What is the meaning of the different types of arrows/connections that you see in this area?
:::

:::{solution} db-s2a-a1-q8
:class: dropdown
Path 1: mTOR phosphorylates the ribosomal protein S6 kinases, which activate ribosomal protein S6 and EIF4B, leading to cell growth and protein synthesis.

Path 2: mTOR phosphorylates EIF4EBP1, thereby inhibiting it and releasing the EIF4E proteins, leading to cell growth and protein synthesis (inhibition of an inhibitor).

Interactions with normal arrowheads generally indicate a positive interaction: stimulation or activation. Interactions with a T-bar at their end indicate inhibition.

*Checked 2026-10-23, WikiPathways WP3932 (last edited 2025-11-23).*
:::

## Assignment 2: Your version's compound in ChEBI and PubChem

*Time: 15 min.*

Pathways contain not only genes and proteins but also small molecules: hormones, metabolites, drugs. Chemical databases describe these. **ChEBI** (Chemical Entities of Biological Interest, at EMBL-EBI) is a curated dictionary of small molecules, with their structure and their biological *roles*. **PubChem** (at NCBI) is a very large collection that gathers information from hundreds of sources, including bioactivity, safety and literature. Use the compound and pathway of your version (see the table above).

:::{exercise} Question 1
:label: db-s2a-a2-q1
:nonumber:
Open the pathway of your version and click the compound. Which database does the pathway use to identify it, and what is the identifier?
:::

:::{solution} db-s2a-a2-q1
:class: dropdown
- **A — Estrogens (WP4194):** ChEBI, CHEBI:50114.
- **B — Creatine (WP5190):** ChEBI, CHEBI:16919.
- **C — Calcitriol (WP1531):** HMDB (Human Metabolome Database), HMDB0001903. Not every pathway uses ChEBI; you will need to translate this identifier in the next question.

```{figure} figures/2a-train-A-wp4194.png
:name: db-fig-2a-train-A-wp4194
:alt: Version A: WP4194, Estrogens ringed.

Version A: WP4194, Estrogens ringed. Figure from WikiPathways WP4194 (CC0).
```

```{figure} figures/2a-train-B-wp5190.png
:name: db-fig-2a-train-B-wp5190
:alt: Version B: WP5190, creatine ringed.

Version B: WP5190, creatine ringed. Figure from WikiPathways WP5190 (CC0).
```

```{figure} figures/2a-train-C-wp1531.png
:name: db-fig-2a-train-C-wp1531
:alt: Version C: WP1531, calcitriol ringed.

Version C: WP1531, calcitriol ringed. Figure from WikiPathways WP1531 (CC0).
```

*Checked 2026-10-23, WikiPathways.*
:::

:::{exercise} Question 2
:label: db-s2a-a2-q2
:nonumber:
Find your compound in ChEBI (<https://www.ebi.ac.uk/chebi/>). Version A: CHEBI:50114 does not describe one molecule; find out what it is, then look up **estradiol**. Version C: search ChEBI for **calcitriol**. Give the ChEBI name, identifier and molecular formula, and two of the roles ChEBI lists.
:::

:::{solution} db-s2a-a2-q2
:class: dropdown
- **A:** CHEBI:50114 is **estrogen**, a *role* that ChEBI defines as a hormone that stimulates or controls female sex characteristics by binding to oestrogen receptors. It has no structure of its own; many molecules have this role (estrone, estradiol, estriol and synthetic ones). The pathway box "Estrogens" stands for the whole group. The main human estrogen is **17β-estradiol**, CHEBI:16469, C₁₈H₂₄O₂. Roles include *estrogen*, *human metabolite* and *geroprotector*.
- **B:** **creatine**, CHEBI:16919, C₄H₉N₃O₂, defined as a glycine derivative. Roles include *human metabolite*, *nutraceutical*, *neuroprotective agent* and *geroprotector*.
- **C:** **calcitriol**, CHEBI:17823, C₂₇H₄₄O₃, the active form of vitamin D₃. Roles include *hormone*, *bone density conservation agent* and *human metabolite*.

```{figure} figures/2a-train-A-chebi.png
:name: db-fig-2a-train-A-chebi
:alt: Version A: ChEBI CHEBI:16469, estradiol.

Version A: ChEBI CHEBI:16469, estradiol. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

```{figure} figures/2a-train-B-chebi.png
:name: db-fig-2a-train-B-chebi
:alt: Version B: ChEBI CHEBI:16919, creatine.

Version B: ChEBI CHEBI:16919, creatine. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

```{figure} figures/2a-train-C-chebi.png
:name: db-fig-2a-train-C-chebi
:alt: Version C: ChEBI CHEBI:17823, calcitriol.

Version C: ChEBI CHEBI:17823, calcitriol. Screenshot of ChEBI, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, ChEBI.*
:::

:::{exercise} Question 3
:label: db-s2a-a2-q3
:nonumber:
Look up the same compound in PubChem. What is its PubChem CID? Give one kind of information that PubChem shows and ChEBI does not.
:::

:::{solution} db-s2a-a2-q3
:class: dropdown
- **A:** estradiol, CID 5757.
- **B:** creatine, CID 586.
- **C:** calcitriol, CID 5280453.

PubChem gathers far more, from many sources. Examples: drug and medication information, pharmacology, safety and hazards (GHS classification), toxicity, bioassay results, patents, vendors and literature counts. ChEBI is smaller and curated, and focuses on what the molecule *is* and which roles it has. The two complement each other: ChEBI for a precise, curated identity; PubChem for everything that has been reported about the compound.

*Checked 2026-10-23, PubChem.*
:::

:::{exercise} Question 4
:label: db-s2a-a2-q4
:nonumber:
Read the ChEBI definition and roles of your compound (version A: of estradiol). How does it connect to the tutorial case of your version?
:::

:::{solution} db-s2a-a2-q4
:class: dropdown
- **A (case 5):** estradiol is the main estrogen. In puberty it stimulates the growth spurt (via GH and IGF1, as in the pathway) and later closes the growth plates. Its role as *geroprotector* links to the ageing cases.
- **B (case 4):** creatine stores energy in muscle as phosphocreatine (also in the pathway), which regenerates ATP during short bursts of contraction. That is why it is used as a supplement (*nutraceutical*). Its breakdown product creatinine (CHEBI:16737) is used clinically as a marker of kidney function and muscle mass.
- **C (case 3):** calcitriol is made in the kidney from calcidiol and increases calcium uptake from the gut. Calcium is needed for bone mineralisation, hence the role *bone density conservation agent*.
:::

## Assignment 3: Genetic and functional information on your gene from NCBI

*Time: 30 min.*

We continue with a database with more details on genes and their function: **NCBI Gene**, at the National Center for Biotechnology Information. Open the NCBI Gene page of your version's gene (see the table above). Version A can also reach it through the link on WikiPathways.

NCBI Gene integrates information from a wide range of species. A record on a gene may include nomenclature, Reference Sequences (RefSeqs), maps, pathways, variations, phenotypes, and links to genome-, phenotype-, and locus-specific resources worldwide.

:::{exercise} Question 1
:label: db-s2a-a3-q1
:nonumber:
What is the NCBI Gene identifier, official symbol and full name of your gene?
:::

:::{solution} db-s2a-a3-q1
:class: dropdown
- **A:** 3479, IGF1, *insulin like growth factor 1*.
- **B:** 2660, MSTN, *myostatin*.
- **C:** 2261, FGFR3, *fibroblast growth factor receptor 3*.

*Checked 2026-10-23, NCBI Gene.*
:::

:::{exercise} Question 2
:label: db-s2a-a3-q2
:nonumber:
What are other names (aliases) of this gene? Compare them with the synonyms Ensembl lists. Version A: compare with your preparation (assignment 4, question 1). Versions B and C: open the gene in Ensembl ([MSTN](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000138379), [FGFR3](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000068078)). Are there differences? How could differences in names affect your searches in other databases, and how do databases try to limit this problem?
:::

:::{solution} db-s2a-a3-q2
:class: dropdown
- **A — IGF1:** NCBI: IGF, IGF-I, IGFI, MGF. Ensembl: IGF, IGF-I, IGF1A, IGFI.
- **B — MSTN:** NCBI: GDF8, MSLHP. Ensembl: GDF8. UniProt even uses GDF8 as the main name ("Growth/differentiation factor 8").
- **C — FGFR3:** NCBI: ACH, CD333, CEK2, HSFGFR3EX, JTK4. Ensembl: ACH, CD333, CEK2, JTK4.

The lists overlap but are not identical, and formatting differs (IGF-I vs IGFI). Using alternative names inconsistently can lead to missed literature, wrong search results, or confusion between genes or species. Databases limit this by providing synonym lists, using stable identifiers (NCBI Gene IDs, Ensembl IDs, HGNC IDs) and cross-linking to each other. Stable identifiers remove the ambiguity, which is why they are essential in bioinformatics.

*Checked 2026-10-23, NCBI Gene and Ensembl.*
:::

:::{exercise} Question 3
:label: db-s2a-a3-q3
:nonumber:
On which chromosome is your gene located? How many exons does the gene have (total, regardless of transcript)?
:::

:::{solution} db-s2a-a3-q3
:class: dropdown
- **A — IGF1:** chromosome 12 (12q23.2); 7 exons.
- **B — MSTN:** chromosome 2 (2q32.2); 3 exons.
- **C — FGFR3:** chromosome 4 (4p16.3); 19 exons.

*Checked 2026-10-23, NCBI Gene.*
:::

:::{exercise} Question 4
:label: db-s2a-a3-q4
:nonumber:
Explain what RefSeq identifiers are, and name the main categories relevant for genes, transcripts and proteins. (Start with <https://en.wikipedia.org/wiki/RefSeq>.)
:::

:::{solution} db-s2a-a3-q4
:class: dropdown
The Reference Sequence (RefSeq) database is an open-access, annotated and curated collection of nucleotide sequences (DNA, RNA) and their protein products. It aims to provide one record for each natural biological molecule (DNA, RNA or protein) for major organisms, with separate but linked records for the genomic DNA, the transcripts and the proteins.

The prefix tells you the type of record:

- **NG\_**: genomic region of a gene (RefSeqGene).
- **NC\_**: complete chromosome.
- **NM\_**: messenger RNA (curated).
- **NR\_**: non-coding RNA (curated), not translated into protein.
- **NP\_**: protein (curated).
- **XM\_** / **XP\_**: predicted (model) mRNA and protein, made by computational annotation and not yet curated.
:::

:::{exercise} Question 5
:label: db-s2a-a3-q5
:nonumber:
Give the RefSeq identifier of the gene (NG\_), and the RefSeq IDs of the **MANE Select** transcript (NM\_) and its protein (NP\_). What is the name of that protein? (Hint: use the table of contents to go to the *NCBI Reference Sequences (RefSeq)* section. The classic gene page does not label which transcript is MANE Select; find out via the **Try the new Transcript table** link, or via the RefSeq match column of the Ensembl *Transcripts table*.)

Genomic RefSeq ID:

mRNA RefSeq ID:

Protein RefSeq ID:

Protein name:
:::

:::{solution} db-s2a-a3-q5
:class: dropdown
| | A — IGF1 | B — MSTN | C — FGFR3 |
|---|---|---|---|
| Genomic (NG\_) | NG_011713.1 | NG_009800.1 | NG_012632.1 |
| mRNA, MANE Select (NM\_) | NM_000618.5 | NM_005259.3 | NM_000142.5 |
| Protein (NP\_) | NP_000609.1 | NP_005250.1 | NP_000133.1 |
| Protein name | insulin-like growth factor 1 isoform 4 preproprotein | growth/differentiation factor 8 preproprotein | fibroblast growth factor receptor 3 isoform 1 precursor |

The MANE Select transcript is the same one Ensembl flags as MANE Select (2A preparation, assignment 4). Note that for IGF1 this protein has 153 amino acids, while UniProt's canonical IGF1 sequence has 195. Different databases choose different reference forms.

```{figure} figures/2a-train-A-ncbi-refseq.png
:name: db-fig-2a-train-A-ncbi-refseq
:alt: Version A: NCBI Gene IGF1, RefSeq section.

Version A: NCBI Gene IGF1, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} figures/2a-train-B-ncbi-refseq.png
:name: db-fig-2a-train-B-ncbi-refseq
:alt: Version B: NCBI Gene MSTN, RefSeq section.

Version B: NCBI Gene MSTN, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} figures/2a-train-C-ncbi-refseq.png
:name: db-fig-2a-train-C-ncbi-refseq
:alt: Version C: NCBI Gene FGFR3, RefSeq section.

Version C: NCBI Gene FGFR3, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-24, NCBI RefSeq (annotation RS_2025_08).*
:::

:::{exercise} Question 6
:label: db-s2a-a3-q6
:nonumber:
How many transcripts (splice variants) are listed in the RefSeq section for your gene? How many are curated (NM\_ / NR\_) and how many predicted (XM\_)? (The RefSeq section lists the transcripts directly. The **Try the new Transcript table** link at the top of that section leaves NCBI Gene for the NCBI Datasets page, which counts differently. Answer from the RefSeq section itself, and say which route you used.)
:::

:::{solution} db-s2a-a3-q6
:class: dropdown
- **A — IGF1:** 7 curated NM\_ and 3 predicted XM\_ on the reference genome GRCh38.
- **B — MSTN:** 1: a single curated NM\_, no predicted ones.
- **C — FGFR3:** 5 curated NM\_ and 1 curated NR\_ (non-coding), plus 12 predicted XM\_ on GRCh38 (for 10 predicted isoforms, X1–X10; some isoforms are encoded by two XM\_ records).

Careful: the predicted models are listed once for each genome assembly NCBI annotates (the reference GRCh38 and the newer, complete T2T-CHM13 genome), so a page may show each XM\_ model twice (for IGF1: 6 instead of 3). Both counts are acceptable if you say what you counted.

⚠️ **Route-dependent and release-volatile.** The *Try the new Transcript table* link leaves NCBI Gene for NCBI Datasets, which counts differently. Both are defensible; say which page you read it from. The number of predicted XM\_ models in particular changes with each annotation release.

*Checked 2026-10-24, NCBI RefSeq annotation RS_2025_08.*
:::

:::{exercise} Question 7
:label: db-s2a-a3-q7
:nonumber:
Go to the **Expression** section and select the **adult** dataset in the drop-down at the top of the section (HPA RNA-seq normal tissues). In which tissues is your gene expressed most (top 2)? Is that what you would expect from its function?
:::

:::{solution} db-s2a-a3-q7
:class: dropdown
- **A — IGF1:** endometrium and fat (then prostate and liver). Most circulating IGF-1 is made by the liver in response to growth hormone, but IGF-1 also acts locally, in many tissues.
- **B — MSTN:** oesophagus and brain, but all values are very low (below 1 TPM). The tissue where myostatin matters most, **skeletal muscle**, is *not among the 27 tissues* in this dataset. An expression chart can only show the tissues that were sampled: no signal is not the same as no expression.
- **C — FGFR3:** skin, by far (about 120 TPM), then oesophagus and brain. Cartilage and the growth plate, where FGFR3 controls bone growth, are not in the dataset.

⚠️ **Release-volatile.** *Checked 2026-10-23, NCBI Gene, HPA RNA-seq normal tissues (PRJEB4337).*

```{figure} figures/2a-train-A-ncbi-expression.png
:name: db-fig-2a-train-A-ncbi-expression
:alt: Version A: NCBI Gene IGF1, adult expression.

Version A: NCBI Gene IGF1, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} figures/2a-train-B-ncbi-expression.png
:name: db-fig-2a-train-B-ncbi-expression
:alt: Version B: NCBI Gene MSTN, adult expression.

Version B: NCBI Gene MSTN, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} figures/2a-train-C-ncbi-expression.png
:name: db-fig-2a-train-C-ncbi-expression
:alt: Version C: NCBI Gene FGFR3, adult expression.

Version C: NCBI Gene FGFR3, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 8
:label: db-s2a-a3-q8
:nonumber:
Now switch the drop-down to the **fetal** dataset (this is the one the section may open on by default). In which organ is your gene expressed most during human fetal development?
:::

:::{solution} db-s2a-a3-q8
:class: dropdown
- **A — IGF1:** lung (week 10). IGF1 is important for lung maturation and branching morphogenesis.
- **B — MSTN:** adrenal gland (week 10), but again at trace level; the fetal dataset has no skeletal muscle either.
- **C — FGFR3:** lung and intestine (weeks 15–20).

*Checked 2026-10-23, NCBI Gene, fetal tissue RNA-seq (PRJNA270632).*
:::

:::{exercise} Question 9
:label: db-s2a-a3-q9
:nonumber:
Scroll down to the **Phenotypes** section. Which phenotype(s) are associated with your gene? Is this what you would expect from its function? What is the OMIM ID of the main phenotype?
:::

:::{solution} db-s2a-a3-q9
:class: dropdown
- **A — IGF1:** growth delay due to insulin-like growth factor I deficiency, OMIM 608747. Expected: IGF1 is essential for normal linear growth and skeletal development.
- **B — MSTN:** muscle hypertrophy, OMIM 614160 (autosomal recessive). OMIM marks it "?Muscle hypertrophy": the question mark means the link between gene and phenotype is still provisional. Expected, because myostatin is a *negative* regulator of muscle growth: losing it gives more muscle. The same happens in "double-muscled" cattle breeds and in mice without myostatin.
- **C — FGFR3:** achondroplasia, OMIM 100800 (autosomal dominant), the most common form of dwarfism, plus related skeletal dysplasias (hypochondroplasia, thanatophoric dysplasia types I and II, SADDAN, Muenke and Crouzon syndrome with acanthosis nigricans) and several somatic cancers (bladder, cervical, colorectal). Expected, because FGFR3 *slows down* chondrocyte proliferation in the growth plate: activating mutations such as Gly380Arg make it overactive, and bone growth is reduced.

*Checked 2026-10-23, NCBI Gene and ClinVar; OMIM numbers checked by hand 2026-10-24.*
:::

:::{exercise} Question 10
:label: db-s2a-a3-q10
:nonumber:
Move to the **Pathways from PubChem** section. Which pathway databases are included in the list, and which one provides the most entries? Is a WikiPathways pathway you have used today included? If so, what is its identifier? (Hint: the widget is a small embedded panel; type `WP` plus the number into its own search box rather than scrolling.)
:::

:::{solution} db-s2a-a3-q10
:class: dropdown
The list combines Reactome and WikiPathways, plus PANTHER for IGF1 and the Pathway Interaction Database and PathBank for FGFR3; for all three genes most entries come from WikiPathways. Versions A and C will find WP3932 (assignment 1), because both IGF1 and FGFR3 are in it; version A also finds WP4194 (assignment 2). None of today's pathways contains MSTN, but version B will find WP3850 (*Factors and pathways affecting insulin-like growth factor (IGF1)-Akt signaling*), in which myostatin acts on IGF1-Akt signalling through its receptor ACVR2B. The number of pathways grows as pathway databases grow.

⚠️ **Release-volatile.** *Checked 2026-10-28, WikiPathways and PubChem pathway data; the PubChem widget itself to be re-checked.*
:::

:::{exercise} Question 11
:label: db-s2a-a3-q11
:nonumber:
**Compare with another version.** Put your answers to questions 6, 7 and 9 next to those of a classmate who chose a different version (or next to your own answers for a second version). Which gene has the most transcripts and which the fewest? Which phenotype comes from *too little* activity of the gene product, and which from *too much*?
:::

:::{solution} db-s2a-a3-q11
:class: dropdown
- **Transcripts:** MSTN has a single RefSeq transcript, IGF1 7 curated (plus predicted models) and FGFR3 6 curated (plus predicted models). In Ensembl: 2, 15 and 24. A small, simple gene versus genes with many alternative forms.
- **Too little:** IGF1 deficiency (loss of a growth *stimulator*, so less growth) and MSTN-related muscle hypertrophy (loss of a growth *inhibitor*, so more muscle).
- **Too much:** achondroplasia. An activating FGFR3 mutation over-activates a growth *inhibitor*, so less bone growth.

Together they show that growth is set by a balance of stimulating and inhibiting signals, and that a mutation's effect depends on whether it removes or enhances the function of the protein.
:::
