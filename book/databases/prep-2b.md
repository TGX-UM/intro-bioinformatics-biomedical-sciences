(db-prep-2b)=
# Practical 2B: preparation

*Time: about 2 hours, before the 2B computer session.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

In the BBS2002 case 12 you study the hallmarks of cancer. Databases provide a reliable source of
up-to-date information and can complement knowledge in text books and other literature
sources.

In this preparation you revisit the genomic database Ensembl, study one variant of the APC gene
in the variant databases dbSNP and ClinVar, and then explore a protein database (UniProt).
There are three assignments.

*Background: the [Reference guide](guide/index.md) has one page per database.*

## Assignment 1: Important biological databases

First, watch the following videos posted on YouTube. Note that not all databases we will use during this practical have a tutorial video, and not all examples of usage covered in the videos will be discussed during the practicals.

1.  Uniprot intro: <https://www.youtube.com/watch?v=OwOJmKmc7VM> (2:34)

2.  UniProtKB: <https://www.youtube.com/watch?v=yp1O1gDK8oA> (1:55)

3.  UniProt exploration: <https://www.youtube.com/watch?v=BHu88Sv--mc> (3:15)

Second, read the abstract and introduction section of this paper on gene and protein databases: <https://dx.doi.org/10.1091%2Fmbc.E13-10-0602>.

## Assignment 2: the APC gene and its variants

This assignment has two halves. First you place the gene, in Ensembl. Then you study one variant in it, in dbSNP, and check what Ensembl says about the same variant.

A word on why it is split that way. Until 2026, all of this was done in Ensembl. Ensembl has since rebuilt its website. The new site still shows a variant, its consequence for each transcript and its frequency in populations, but no longer the clinical interpretation (pathogenic or benign) or the gene-wide variant table this assignment used to rely on. That information now has to come from **dbSNP** and **ClinVar**, at NCBI, which you will also use in the computer session.

That is worth noticing in its own right. Databases are rebuilt, and when they are, information moves or is dropped. Knowing which resource is the primary home for a kind of data (variant interpretations in ClinVar, proteins in UniProt, pathways in WikiPathways) is more durable than knowing one website's menus.

### Part A: the APC gene in Ensembl

Open the human APC gene: <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000134982>

:::{exercise} Question 1
:label: db-p2b-a2-q1
:nonumber:
What is the full gene name, and what other names does Ensembl list for it?
:::

:::{solution} db-p2b-a2-q1
:class: dropdown
Name: *APC regulator of WNT signaling pathway*. Other names listed: DP2, DP2.5, DP3, PPP1R46.

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

:::{exercise} Question 2
:label: db-p2b-a2-q2
:nonumber:
What is the chromosomal position (chromosome, location and strand) of APC? How does the strand compare with IGF1 from practical 2A?
:::

:::{solution} db-p2b-a2-q2
:class: dropdown
Chromosome 5: 112,707,452–112,846,239, forward strand, on assembly GRCh38. IGF1 is on the reverse strand of chromosome 12. Strand simply says which of the two DNA strands carries the coding sequence; it has no bearing on how important or how active a gene is.

```{figure} figures/2b-prep-ens-apc.png
:name: db-fig-2b-prep-ens-apc
:alt: Ensembl, APC gene page.

Ensembl, APC gene page. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

:::{exercise} Question 3
:label: db-p2b-a2-q3
:nonumber:
Switch to the **Transcripts table** view. How many transcripts does APC have, and how many are protein coding? Find transcript **ENST00000257430**: how long is the protein it encodes, which flags does it carry, and is it the longest protein of the gene?
:::

:::{solution} db-p2b-a2-q3
:class: dropdown
33 transcripts, of which 23 are protein coding (the others are 9 nonsense-mediated-decay transcripts and 1 retained intron). ENST00000257430.9 encodes the 2,843-amino-acid APC protein. It carries the flags **MANE Select** and **Ensembl canonical**: it is the reference transcript that Ensembl and NCBI agree on (it matches RefSeq `NM_000038.6`), and the one this and the following assignments use. It is not the longest: three other transcripts encode 2,861 amino acids.

⚠️ **Release-volatile** — Ensembl's count was 10 transcripts on 31 August 2026 and 33 on 22 October, under the same release label. Report the count with the gene version shown on the page (here ENSG00000134982.21) and the date.

```{figure} figures/2b-prep-ens-apc-tx.png
:name: db-fig-2b-prep-ens-apc-tx
:alt: Ensembl, APC Transcripts table (first rows; MANE Select ringed).

Ensembl, APC Transcripts table (first rows; MANE Select ringed). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

### Part B: the variant rs137854573 in dbSNP

Open <https://www.ncbi.nlm.nih.gov/snp/rs137854573>.

:::{exercise} Question 4
:label: db-p2b-a2-q4
:nonumber:
Which reference allele and which alternative alleles are reported at this position, and on which chromosome and coordinate (GRCh38)?
:::

:::{solution} db-p2b-a2-q4
:class: dropdown
Reference C, with alternative alleles A, G and T, at chr5:112,828,889 on GRCh38 (`NC_000005.10`). More than one alternative allele at a single position is normal, and it matters for every question below.

```{figure} figures/2b-prep-dbsnp-summary.png
:name: db-fig-2b-prep-dbsnp-summary
:alt: dbSNP rs137854573, summary.

dbSNP rs137854573, summary. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5
:label: db-p2b-a2-q5
:nonumber:
Open the **Variant Details** tab. For transcript `NM_000038.6`, what change does each alternative allele cause at the amino-acid level, and at which position in the protein?
:::

:::{solution} db-p2b-a2-q5
:class: dropdown
All three changes fall on codon **554**, which encodes arginine (R):

| Allele | Codon | Protein change | Consequence |
|---|---|---|---|
| C→T | Cga → Tga | R554\* | stop gained (nonsense) |
| C→G | Cga → Gga | R554G | missense |
| C→A | Cga → Aga | R554R | synonymous |

One position, three alleles, three different consequences.

```{figure} figures/2b-prep-dbsnp-details.png
:name: db-fig-2b-prep-dbsnp-details
:alt: dbSNP rs137854573, Variant Details: the three alleles on NM_000038.6.

dbSNP rs137854573, Variant Details: the three alleles on NM_000038.6. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5b
:label: db-p2b-a2-q5b
:nonumber:
Now open the same variant in **Ensembl**: type `rs137854573` into the search box at <https://www.ensembl.org/search> (if the box is greyed out, first add Human GRCh38.p14 under **Find a genome**) and open the result in the Feature explorer. Ensembl shows one alternative allele at a time; switch between them and open **Transcript consequences**. Does Ensembl give the same consequence for each allele on the MANE Select transcript as dbSNP? What does Ensembl show in the panels **Allele frequency** and **Variant phenotypes**?
:::

:::{solution} db-p2b-a2-q5b
:class: dropdown
Yes. On ENST00000257430.9 (MANE Select, the Ensembl equivalent of `NM_000038.6`) Ensembl gives A = synonymous_variant, G = missense_variant, T = stop_gained, all at position 1,660 of the coding sequence, in coding exon 13 of 15. That is codon 554, as in dbSNP. The header bar shows "Most severe consequence: stop_gained", which summarises all three alleles together.

The Allele frequency tile reads "unknown", but the panel itself shows the T allele once in gnomAD exomes v4.1 (global frequency 6.8 × 10⁻⁷); A and G have no data. The variant is extremely rare. Variant phenotypes is 0: the new Ensembl website carries no clinical interpretations, so for the question "is this allele harmful?" you need dbSNP and ClinVar (next questions).

```{figure} figures/2b-prep-ens-var-T.png
:name: db-fig-2b-prep-ens-var-T
:alt: Ensembl, rs137854573 allele T: stop_gained.

Ensembl, rs137854573 allele T: stop_gained. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

```{figure} figures/2b-prep-ens-var-G.png
:name: db-fig-2b-prep-ens-var-G
:alt: Ensembl, rs137854573 allele G: missense.

Ensembl, rs137854573 allele G: missense. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-28, Ensembl gene ENSG00000134982.21 (variant data from dbSNP 157).*
:::

:::{exercise} Question 6
:label: db-p2b-a2-q6
:nonumber:
What would the C→T allele do to the resulting protein, and why does that matter for APC specifically?
:::

:::{solution} db-p2b-a2-q6
:class: dropdown
It introduces a premature stop codon at residue 554 of a 2,843-residue protein, so roughly 80% of APC is never made. The domains APC needs for its tumour-suppressor role — the β-catenin binding and down-regulation regions, the axin-binding SAMP repeats, the microtubule-binding C-terminus — all lie downstream of residue 554 and are lost. The truncated product cannot down-regulate β-catenin, so Wnt signalling stays on.
:::

:::{exercise} Question 7
:label: db-p2b-a2-q7
:nonumber:
Still in **Variant Details**, compare `NM_000038.6` with `NM_001127511.3`, `NM_001354896.2` and `NM_001354897.2`. The same genomic change is reported at a different protein position in each. Why?
:::

:::{solution} db-p2b-a2-q7
:class: dropdown
Codon 554 in `NM_000038.6` is codon 536 in `NM_001127511.3`, 572 in `NM_001354896.2` and 564 in `NM_001354897.2`. The transcripts differ in which exons they include and where translation starts, so the same base sits a different number of codons from the start of each coding sequence.

The lesson is that a protein-level description such as "R554\*" is meaningless without saying which transcript it is numbered against. This is exactly why HGVS notation is always written with its reference sequence, as `NM_000038.6:c.1660C>T`.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 8
:label: db-p2b-a2-q8
:nonumber:
Open the **Clinical Significance** tab. Which clinical significances are reported, and to which allele does each belong? Which phenotypes are named?
:::

:::{solution} db-p2b-a2-q8
:class: dropdown
Two, and they disagree because they describe different alleles: the C→T (stop-gained) allele is **pathogenic** (multiple submitters, no conflicts), and the C→A (synonymous) allele is **likely benign**. The C→G (missense) allele has no clinical classification at all. Phenotypes reported for the pathogenic allele include familial adenomatous polyposis 1 (the main one), hereditary desmoid disease, gastric cancer, susceptibility to colorectal cancer and hereditary cancer-predisposing syndrome; the likely-benign classification is for hereditary cancer-predisposing syndrome.

Reading "pathogenic" off the variant without checking which allele it refers to is the mistake this question exists to prevent.

⚠️ **Release-volatile** — ClinVar submissions accumulate. *Checked 2026-10-23, ClinVar (live) and dbSNP build 157.*

```{figure} figures/2b-prep-dbsnp-clinical.png
:name: db-fig-2b-prep-dbsnp-clinical
:alt: dbSNP rs137854573, Clinical Significance per allele.

dbSNP rs137854573, Clinical Significance per allele. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 9
:label: db-p2b-a2-q9
:nonumber:
What kinds of evidence support these classifications? Follow one link through to ClinVar and say who submitted it and on what basis.
:::

:::{solution} db-p2b-a2-q9
:class: dropdown
Each ClinVar record carries a submitter, a review status (the star rating), a condition and supporting evidence — most commonly clinical testing by a diagnostic laboratory, sometimes with literature citations. Answers should name a submitter and its review status rather than just repeating "pathogenic".

An assertion in a database is only as good as who made it and why. The star rating exists precisely so you can tell a single unreviewed submission from an expert-panel consensus.
:::

:::{exercise} Question 10
:label: db-p2b-a2-q10
:nonumber:
A variant that introduces a premature stop codon is called a **protein-truncating variant** (PTV). Which molecular consequences count as protein-truncating, and what do they have in common?
:::

:::{solution} db-p2b-a2-q10
:class: dropdown
Nonsense (stop-gained), frameshift, and variants disrupting the canonical splice donor or acceptor sites. All three cause the ribosome to stop early or to read the wrong frame, so the protein is truncated or garbled from that point on. Many such transcripts are additionally destroyed by nonsense-mediated decay before much protein is made.
:::

:::{exercise} Question 11
:label: db-p2b-a2-q11
:nonumber:
Why are PTVs in APC so often associated with disease, when missense changes in the same gene frequently are not?
:::

:::{solution} db-p2b-a2-q11
:class: dropdown
APC is a tumour suppressor, and its function depends on a long C-terminal half. Truncation removes that half wholesale, so almost any early PTV destroys function — a large target with a predictable outcome. A missense change swaps one amino acid, which may sit in a critical site or may be tolerated entirely, so its effect has to be argued case by case.

This is also why germline PTVs in APC cluster in familial adenomatous polyposis, and why the position of a truncation predicts how severe the polyposis is.
:::

## Assignment 3: the APC protein in UniProt

Now we turn to the UniProt database, to find more information about the function and structure of the protein encoded by the gene from the second assignment. First, go to the UniProt page of the human protein of APC (<https://www.uniprot.org/uniprotkb/P25054/entry>).

:::{exercise} Question 1
:label: db-p2b-a3-q1
:nonumber:
What is the UniProt name and identifier of the human APC protein, and what is the entry’s review status?
:::

:::{solution} db-p2b-a3-q1
:class: dropdown
The human APC protein is listed as *Adenomatous polyposis coli protein*, with UniProt identifier P25054. The entry is reviewed (Swiss-Prot), meaning it has undergone expert curation.

```{figure} figures/2b-prep-uni-names.png
:name: db-fig-2b-prep-uni-names
:alt: UniProt P25054, entry header.

UniProt P25054, entry header. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

The page starts off with a concise description of the function of the protein, supported by references.

:::{exercise} Question 2
:label: db-p2b-a3-q2
:nonumber:
How many references are supporting the function description, and which one is most recent?
:::

:::{solution} db-p2b-a3-q2
:class: dropdown
UniProt cites six publications supporting APC’s functional description. The most recent reference is from 2010 (Zaoui et al.).

```{figure} figures/2b-prep-uni-function.png
:name: db-fig-2b-prep-uni-function
:alt: UniProt P25054, Function.

UniProt P25054, Function. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Further on, in the “Miscellaneous” paragraph at the bottom of the *Function* section, some generic information on the types and positions of the mutations is given.

:::{exercise} Question 3
:label: db-p2b-a3-q3
:nonumber:
Does the information on mutations given by UniProt correspond to what you found for rs137854573 in dbSNP and ClinVar (assignment 2, question 8)?
:::

:::{solution} db-p2b-a3-q3
:class: dropdown
Yes. Both link APC mutations to familial adenomatous polyposis (FAP) and colorectal cancer, and UniProt notes that most disease mutations truncate the protein, as the pathogenic C→T allele (R554\*) does. UniProt describes the effects at the protein level, while dbSNP and ClinVar describe single variants and their clinical classification, so the details differ but the overall picture agrees.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Further on, information on the GO annotations for the protein is given, based on Molecular function and Biological process (cellular component are listed in a graphical overview further down on the page). Click the small “i” next to “GO annotations” for an explanation on what GO (Gene Ontology) is.

:::{exercise} Question 4
:label: db-p2b-a3-q4
:nonumber:
In the overview of terms in the side-scrolling window, click the “All Biological Process” box (if a “Slimming set” drop-down is shown above the ribbon, leave it at its default) to filter the table for processes in which APC is involved. What is the evidence type and PubMed ID for the GO Biological Process annotation “DNA damage response”?
:::

:::{solution} db-p2b-a3-q4
:class: dropdown
The annotation is supported by experimental evidence (IDA: Inferred from Direct Assay). The associated PubMed ID is 14728717.

```{figure} figures/2b-prep-uni-go.png
:name: db-fig-2b-prep-uni-go
:alt: UniProt P25054, GO annotations.

UniProt P25054, GO annotations. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 5
:label: db-p2b-a3-q5
:nonumber:
Moving to the section “Subcellular Location”: Which general subcellular locations are given for this protein by “UniProt annotation”? How many references are given (in total), for these annotations?
:::

:::{solution} db-p2b-a3-q5
:class: dropdown
UniProt annotation gives: cell junction (adherens junction), cytoskeleton, lamellipodium, ruffle membrane, cytoplasm and cell membrane.

Count the publications shown next to these locations: 1 + 2 + 1 + 1 + 1 + 3 = 9 (12 if you also count the 3 under the Note), from 5 distinct papers. The number depends on whether you count each citation or each distinct paper: the same publication can support several locations. Comparing them by hand is possible by opening each publication box; with a script it can be done automatically, which is outside this practical.

```{figure} figures/2b-prep-uni-location.png
:name: db-fig-2b-prep-uni-location
:alt: UniProt P25054, Subcellular Location.

UniProt P25054, Subcellular Location. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-28, UniProt release 2026_03.*
:::

:::{exercise} Question 6
:label: db-p2b-a3-q6
:nonumber:
Which of these UniProt annotations overlap with the subcellular locations given for this protein by the GO cellular-component annotation (Hint: click the second tab, labelled “GO Annotation”, next to the cellular drawing)? Which major organelle is annotated as a cellular location with GO, but is missing with UniProt?
:::

:::{solution} db-p2b-a3-q6
:class: dropdown
Both list adherens junction, ruffle membrane, cytoplasm, (plasma) membrane and lamellipodium. GO adds the **nucleus** (and nucleoplasm), the major organelle missing from the UniProt annotation, plus more specific places and complexes: cytosol, centrosome, kinetochore, tight junctions, the β-catenin destruction complex and the Wnt signalosome. UniProt's "cytoskeleton" appears in GO only as a specific part (the centrosome).

*Checked 2026-10-28, UniProt release 2026_03 (GO cellular component annotations).*
:::

:::{exercise} Question 7
:label: db-p2b-a3-q7
:nonumber:
UniProt and GO list slightly different subcellular locations for APC. What might explain these differences?
:::

:::{solution} db-p2b-a3-q7
:class: dropdown
They use different evidence sources and curation pipelines. UniProt relies on curated literature; GO integrates many databases and inference methods. This can lead to additional or missing terms in one database.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Scrolling further down the page (in the section “Disease & Variants”), we find an overview of involvement of mutations in the protein in human disease. For the next question, we will only focus on the “Familial adenomatous polyposis 1 (FAP1)” disease.

:::{exercise} Question 8
:label: db-p2b-a3-q8
:nonumber:
What is the OMIM identifier for FAP1?
:::

:::{solution} db-p2b-a3-q8
:class: dropdown
175100

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 9
:label: db-p2b-a3-q9
:nonumber:
How many APC variants associated with FAP1 are listed in UniProt, and how many have a dbSNP ID? Use the “Natural variants in FAP1” table inside the Disease & Variants section — not the separate Variant viewer tab, which lists far more.
:::

:::{solution} db-p2b-a3-q9
:class: dropdown
13 variants, of which 6 have a dbSNP ID.

```{figure} figures/2b-prep-uni-disease.png
:name: db-fig-2b-prep-uni-disease
:alt: UniProt P25054, Disease & Variants.

UniProt P25054, Disease & Variants. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

After the disease-associated mutations, a section is presented on processing of the protein (*e.g.* cleaving, amino acid modifications, aka Post Translational Modifications or PTMs).

:::{exercise} Question 10
:label: db-p2b-a3-q10
:nonumber:
Which is the most common modification present for this protein? Why might this modification be an important modification for a protein involved in cell cycle control and signal transduction?
:::

:::{solution} db-p2b-a3-q10
:class: dropdown
The most common modification is phosphorylation of serine (phosphoserine). In APC, serine phosphorylation helps regulate how the protein interacts with partners in the Wnt/β-catenin signaling pathway and supports proper control of cell proliferation. Because APC acts as a tumor suppressor, phosphorylation is important for adjusting its activity within cell-cycle and signaling processes.

```{figure} figures/2b-prep-uni-ptm.png
:name: db-fig-2b-prep-uni-ptm
:alt: UniProt P25054, PTM/Processing.

UniProt P25054, PTM/Processing. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 11
:label: db-p2b-a3-q11
:nonumber:
What is the biological function of this type of modification in general (look up some details for this question outside of UniProt)?
:::

:::{solution} db-p2b-a3-q11
:class: dropdown
Phosphorylation is a reversible post-translational modification in which a phosphate group is added to serine, threonine, or tyrosine residues. It functions as a molecular switch that can rapidly change a protein’s activity, stability, structure, cellular location, or interaction partners. This makes phosphorylation a central mechanism in regulating key cellular processes such as signal transduction, cell growth, and the cell cycle.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Also, scrolling further down, information on interaction partners of the protein is given. Use the Binary interactions figure for the following questions. If it looks crowded, click “Expand table” below the table and compare the “Number of experiments” column.

:::{exercise} Question 12
:label: db-p2b-a3-q12
:nonumber:
Which protein shows the strongest interaction support with APC according to UniProt, and how many experimental observations support this interaction? How many experiments have been performed to establish this interaction (click on the dot to obtain more information)?
:::

:::{solution} db-p2b-a3-q12
:class: dropdown
Some dots are clearly darker in colour than others; these do not actually indicate strength of the interaction, but the colors are based on the number of experiments that support the interaction. The interactions with most support include interactions between APC and CTNB1_HUMAN, AXIN1_HUMAN, and DLG1_HUMAN (compare only the first column with one another, or look into the table below the figure). We will now focus on CTNB1_HUMAN; clicking on the dot reveals there are 22 experiments which confirmed this interaction.

```{figure} figures/2b-prep-uni-interaction.png
:name: db-fig-2b-prep-uni-interaction
:alt: UniProt P25054, Interaction.

UniProt P25054, Interaction. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-28, UniProt release 2026_03.*
:::

Finally, we will have a look at the structural information given in UniProt.

:::{exercise} Question 13
:label: db-p2b-a3-q13
:nonumber:
In general, which secondary protein structural elements exist?
:::

:::{solution} db-p2b-a3-q13
:class: dropdown
Helixes (alpha), turns, beta sheets. (Random coils and “other” structures are also known, but less common).

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Switch to the “Feature viewer” tab at the top of the page. UniProt no longer groups helices, strands and turns under a “Structural features” heading, so use the **PDBe 3D structure coverage** and **AlphaFold** tracks to see which parts of the protein are structured, and look at those parts in the 3D viewer of the *Structure* section on the entry page (helices are drawn as spirals, strands as arrows).

:::{exercise} Question 14
:label: db-p2b-a3-q14
:nonumber:
Which secondary structural element is most common for the APC protein, and where in the protein does it mostly occur?
:::

:::{solution} db-p2b-a3-q14
:class: dropdown
α-helix, by a wide margin, and concentrated in the N-terminal third of the protein. UniProt annotates 41 helices against 4 β-strands and 3 turns; about thirty of those helices fall between residues 328 and 742, which is the armadillo (ARM) repeat region, with a further cluster in the N-terminal oligomerisation region. That is also the part of APC for which experimental structures exist — which is exactly why it is the part with secondary structure annotated.

⚠️ **Note the interface changed.** UniProt removed the “Structural features” grouping from the Feature viewer in late 2025, so a previous year's instruction to open it no longer works. Read the structure from the *PDBe 3D structure coverage* and *AlphaFold* tracks and from the 3D viewer in the *Structure* section instead.

⚠️ **Release-volatile** — the helix count was 36 in 2025.

```{figure} figures/2b-prep-uni-structure.png
:name: db-fig-2b-prep-uni-structure
:alt: UniProt P25054, Structure.

UniProt P25054, Structure. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

## Check yourself

:::{note}
A practice quiz on this preparation will be added on the module page ({ref}`db-practice-quiz`).
:::
