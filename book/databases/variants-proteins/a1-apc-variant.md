(db-p2-a1)=
# Assignment 1: The APC gene and its variants

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

This assignment has two halves. First you place the gene, in Ensembl. Then you study one variant in it, in dbSNP, and check what Ensembl says about the same variant.

A word on why it is split that way. Until 2026, all of this was done in Ensembl. Ensembl has since rebuilt its website. The new site still shows a variant, its consequence for each transcript and its frequency in populations, but no longer the clinical interpretation (pathogenic or benign) or the gene-wide variant table this assignment used to rely on. That information now has to come from **dbSNP** and **ClinVar**, at NCBI, which you will also use in the computer session.

That is worth noticing in its own right. Databases are rebuilt, and when they are, information moves or is dropped. Knowing which resource is the primary home for a kind of data (variant interpretations in ClinVar, proteins in UniProt, pathways in WikiPathways) is more durable than knowing one website's menus.

## Part A: the APC gene in Ensembl

Open the human APC gene: <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000134982>

:::{exercise} Question 1
:label: db-p2a1-q1
:nonumber:
What is the full gene name, and what other names does Ensembl list for it?
:::

:::{solution} db-p2a1-q1
:class: dropdown
Name: *APC regulator of WNT signaling pathway*. Other names listed: DP2, DP2.5, DP3, PPP1R46.

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

:::{exercise} Question 2
:label: db-p2a1-q2
:nonumber:
What is the chromosomal position (chromosome, location and strand) of APC? How does the strand compare with IGF1 from Practical 1?
:::

:::{solution} db-p2a1-q2
:class: dropdown
Chromosome 5: 112,707,452–112,846,239, forward strand, on assembly GRCh38. IGF1 is on the reverse strand of chromosome 12. Strand simply says which of the two DNA strands carries the coding sequence; it has no bearing on how important or how active a gene is.

```{figure} ../figures/2b-prep-ens-apc.png
:name: db-fig-2b-prep-ens-apc
:alt: Ensembl, APC gene page.

Ensembl, APC gene page. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

:::{exercise} Question 3
:label: db-p2a1-q3
:nonumber:
Switch to the **Transcripts table** view. How many transcripts does APC have, and how many are protein coding? Find transcript **ENST00000257430**: how long is the protein it encodes, which flags does it carry, and is it the longest protein of the gene?
:::

:::{solution} db-p2a1-q3
:class: dropdown
33 transcripts, of which 23 are protein coding (the others are 9 nonsense-mediated-decay transcripts and 1 retained intron). ENST00000257430.9 encodes the 2,843-amino-acid APC protein. It carries the flags **MANE Select** and **Ensembl canonical**: it is the reference transcript that Ensembl and NCBI agree on (it matches RefSeq `NM_000038.6`), and the one this and the following assignments use. It is not the longest: three other transcripts encode 2,861 amino acids.

⚠️ **Release-volatile** — Ensembl's count was 10 transcripts on 31 August 2026 and 33 on 22 October, under the same release label. Report the count with the gene version shown on the page (here ENSG00000134982.21) and the date.

```{figure} ../figures/2b-prep-ens-apc-tx.png
:name: db-fig-2b-prep-ens-apc-tx
:alt: Ensembl, APC Transcripts table (first rows; MANE Select ringed).

Ensembl, APC Transcripts table (first rows; MANE Select ringed). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134982.21.*
:::

## Part B: the variant rs137854573 in dbSNP

Open <https://www.ncbi.nlm.nih.gov/snp/rs137854573>.

:::{exercise} Question 4
:label: db-p2a1-q4
:nonumber:
Which reference allele and which alternative alleles are reported at this position, and on which chromosome and coordinate (GRCh38)?
:::

:::{solution} db-p2a1-q4
:class: dropdown
Reference C, with alternative alleles A, G and T, at chr5:112,828,889 on GRCh38 (`NC_000005.10`). More than one alternative allele at a single position is normal, and it matters for every question below.

```{figure} ../figures/2b-prep-dbsnp-summary.png
:name: db-fig-2b-prep-dbsnp-summary
:alt: dbSNP rs137854573, summary.

dbSNP rs137854573, summary. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5
:label: db-p2a1-q5
:nonumber:
Open the **Variant Details** tab. For transcript `NM_000038.6`, what change does each alternative allele cause at the amino-acid level, and at which position in the protein?
:::

:::{solution} db-p2a1-q5
:class: dropdown
All three changes fall on codon **554**, which encodes arginine (R):

| Allele | Codon | Protein change | Consequence |
|---|---|---|---|
| C→T | Cga → Tga | R554\* | stop gained (nonsense) |
| C→G | Cga → Gga | R554G | missense |
| C→A | Cga → Aga | R554R | synonymous |

One position, three alleles, three different consequences.

```{figure} ../figures/2b-prep-dbsnp-details.png
:name: db-fig-2b-prep-dbsnp-details
:alt: dbSNP rs137854573, Variant Details: the three alleles on NM_000038.6.

dbSNP rs137854573, Variant Details: the three alleles on NM_000038.6. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5b
:label: db-p2a1-q5b
:nonumber:
Now open the same variant in **Ensembl**: type `rs137854573` into the search box at <https://www.ensembl.org/search> (if the box is greyed out, first add Human GRCh38.p14 under **Find a genome**) and open the result in the Feature explorer. Ensembl shows one alternative allele at a time; switch between them and open **Transcript consequences**. Does Ensembl give the same consequence for each allele on the MANE Select transcript as dbSNP? What does Ensembl show in the panels **Allele frequency** and **Variant phenotypes**?
:::

:::{solution} db-p2a1-q5b
:class: dropdown
Yes. On ENST00000257430.9 (MANE Select, the Ensembl equivalent of `NM_000038.6`) Ensembl gives A = synonymous_variant, G = missense_variant, T = stop_gained, all at position 1,660 of the coding sequence, in coding exon 13 of 15. That is codon 554, as in dbSNP. The header bar shows "Most severe consequence: stop_gained", which summarises all three alleles together.

The Allele frequency tile reads "unknown", but the panel itself shows the T allele once in gnomAD exomes v4.1 (global frequency 6.8 × 10⁻⁷); A and G have no data. The variant is extremely rare. Variant phenotypes is 0: the new Ensembl website carries no clinical interpretations, so for the question "is this allele harmful?" you need dbSNP and ClinVar (next questions).

```{figure} ../figures/2b-prep-ens-var-T.png
:name: db-fig-2b-prep-ens-var-T
:alt: Ensembl, rs137854573 allele T: stop_gained.

Ensembl, rs137854573 allele T: stop_gained. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

```{figure} ../figures/2b-prep-ens-var-G.png
:name: db-fig-2b-prep-ens-var-G
:alt: Ensembl, rs137854573 allele G: missense.

Ensembl, rs137854573 allele G: missense. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-28, Ensembl gene ENSG00000134982.21 (variant data from dbSNP 157).*
:::

:::{exercise} Question 6
:label: db-p2a1-q6
:nonumber:
What would the C→T allele do to the resulting protein, and why does that matter for APC specifically?
:::

:::{solution} db-p2a1-q6
:class: dropdown
It introduces a premature stop codon at residue 554 of a 2,843-residue protein, so roughly 80% of APC is never made. The domains APC needs for its tumour-suppressor role — the β-catenin binding and down-regulation regions, the axin-binding SAMP repeats, the microtubule-binding C-terminus — all lie downstream of residue 554 and are lost. The truncated product cannot down-regulate β-catenin, so Wnt signalling stays on.
:::

:::{exercise} Question 7
:label: db-p2a1-q7
:nonumber:
Still in **Variant Details**, compare `NM_000038.6` with `NM_001127511.3`, `NM_001354896.2` and `NM_001354897.2`. The same genomic change is reported at a different protein position in each. Why?
:::

:::{solution} db-p2a1-q7
:class: dropdown
Codon 554 in `NM_000038.6` is codon 536 in `NM_001127511.3`, 572 in `NM_001354896.2` and 564 in `NM_001354897.2`. The transcripts differ in which exons they include and where translation starts, so the same base sits a different number of codons from the start of each coding sequence.

The lesson is that a protein-level description such as "R554\*" is meaningless without saying which transcript it is numbered against. This is exactly why HGVS notation is always written with its reference sequence, as `NM_000038.6:c.1660C>T`.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 8
:label: db-p2a1-q8
:nonumber:
Open the **Clinical Significance** tab. Which clinical significances are reported, and to which allele does each belong? Which phenotypes are named?
:::

:::{solution} db-p2a1-q8
:class: dropdown
Two, and they disagree because they describe different alleles: the C→T (stop-gained) allele is **pathogenic** (multiple submitters, no conflicts), and the C→A (synonymous) allele is **likely benign**. The C→G (missense) allele has no clinical classification at all. Phenotypes reported for the pathogenic allele include familial adenomatous polyposis 1 (the main one), hereditary desmoid disease, gastric cancer, susceptibility to colorectal cancer and hereditary cancer-predisposing syndrome; the likely-benign classification is for hereditary cancer-predisposing syndrome.

Reading "pathogenic" off the variant without checking which allele it refers to is the mistake this question exists to prevent.

⚠️ **Release-volatile** — ClinVar submissions accumulate. *Checked 2026-10-23, ClinVar (live) and dbSNP build 157.*

```{figure} ../figures/2b-prep-dbsnp-clinical.png
:name: db-fig-2b-prep-dbsnp-clinical
:alt: dbSNP rs137854573, Clinical Significance per allele.

dbSNP rs137854573, Clinical Significance per allele. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 9
:label: db-p2a1-q9
:nonumber:
What kinds of evidence support these classifications? Follow one link through to ClinVar and say who submitted it and on what basis.
:::

:::{solution} db-p2a1-q9
:class: dropdown
Each ClinVar record carries a submitter, a review status (the star rating), a condition and supporting evidence — most commonly clinical testing by a diagnostic laboratory, sometimes with literature citations. Answers should name a submitter and its review status rather than just repeating "pathogenic".

An assertion in a database is only as good as who made it and why. The star rating exists precisely so you can tell a single unreviewed submission from an expert-panel consensus.
:::

:::{exercise} Question 10
:label: db-p2a1-q10
:nonumber:
A variant that introduces a premature stop codon is called a **protein-truncating variant** (PTV). Which molecular consequences count as protein-truncating, and what do they have in common?
:::

:::{solution} db-p2a1-q10
:class: dropdown
Nonsense (stop-gained), frameshift, and variants disrupting the canonical splice donor or acceptor sites. All three cause the ribosome to stop early or to read the wrong frame, so the protein is truncated or garbled from that point on. Many such transcripts are additionally destroyed by nonsense-mediated decay before much protein is made.
:::

:::{exercise} Question 11
:label: db-p2a1-q11
:nonumber:
Why are PTVs in APC so often associated with disease, when missense changes in the same gene frequently are not?
:::

:::{solution} db-p2a1-q11
:class: dropdown
APC is a tumour suppressor, and its function depends on a long C-terminal half. Truncation removes that half wholesale, so almost any early PTV destroys function — a large target with a predictable outcome. A missense change swaps one amino acid, which may sit in a critical site or may be tolerated entirely, so its effect has to be argued case by case.

This is also why germline PTVs in APC cluster in familial adenomatous polyposis, and why the position of a truncation predicts how severe the polyposis is.
:::
