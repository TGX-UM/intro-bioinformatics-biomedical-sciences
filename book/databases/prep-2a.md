(db-prep-2a)=
# Practical 2A: preparation

*Time: about 2 hours, before the 2A computer session.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

In the BBS2002 cases 4 and 5 you studied signalling processes that promote growth and
development, including Insulin-like Growth Factor 1 (IGF-1). The regulation of growth is a
complex process, in which many molecular interactions are involved. Databases provide a reliable
source of up-to-date information and can complement knowledge in text books and other
literature sources.

In this preparation you use a disease database (OMIM), a pathway database (WikiPathways) and a
genomic database (Ensembl). There are four assignments.

*Background: the [Reference guide](guide/index.md) has one page per database.*

## Assignment 1: Important biological databases

*Time: 30 min.*

First, watch the following videos on several Biological Databases, posted on YouTube. Note that not all databases we will use during this (and the next) practical have a tutorial video, and not all examples of usage covered in the videos will be discussed during the practicals.

1.  NCBI: <https://www.youtube.com/watch?v=paeAAGzckYQ> (7:28)

2.  Ensembl: work through the Ensembl section of EMBL-EBI's *Introductory bioinformatics* pathway, <https://www.ebi.ac.uk/training/online/courses/introductory-bioinformatics-pathway/>. This replaces the old Ensembl video, which shows the website as it was before the 2026 rebuild and would now walk you through pages that no longer exist.

Second, read this short overview of the types of biological database and why they matter: EMBL-EBI's *Bioinformatics for the terrified*, <https://www.ebi.ac.uk/training/online/courses/bioinformatics-terrified/>.

## Assignment 2: genetic variants in the IGF1 gene in OMIM

*Time: 30 min.*

“The somatomedins, or insulin-like growth factors (IGFs), comprise a family of peptides that play important roles in mammalian growth and development.” \[OMIM: 147440\].

Look up the IGF1 gene in OMIM (<https://omim.org/>), a database from Johns Hopkins University that contains expert-curated information on the links between genes and genetic variants and human disease.

:::{exercise} Question 1
:label: db-p2a-a2-q1
:nonumber:
To which disease has this gene been linked? Which identifier is mentioned for this disease (displayed in the table as “Phenotype MIM number”) and with which inheritance pattern?
:::

:::{solution} db-p2a-a2-q1
:class: dropdown
Insulin-like growth factor I deficiency (growth delay due to IGF1 deficiency), phenotype MIM number 608747, inheritance AR = autosomal recessive.

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 2
:label: db-p2a-a2-q2
:nonumber:
What is the alternative name of Insulin-like Growth Factor (IGF1)?
:::

:::{solution} db-p2a-a2-q2
:class: dropdown
SOMATOMEDIN C

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 3
:label: db-p2a-a2-q3
:nonumber:
How many literature references have been used to construct this page for OMIM, and when was the page last updated?
:::

:::{solution} db-p2a-a2-q3
:class: dropdown
Count the numbered entries under REFERENCES; the last update is the top line of *Edit History*. At the time of writing that was 82 references, last updated 10/07/2026 (OMIM writes month/day/year: 7 October 2026).

⚠️ **Release-volatile** — OMIM entries are re-curated. Report what you see.

*Checked 2026-10-24, OMIM checked by hand.*
:::

Open the Table View of Allelic Variants for the IGF1 gene: click **Table View** next to the ALLELIC VARIANTS heading (it is also linked from the left-side menu), or go straight to <https://omim.org/allelicVariants/147440>.

:::{exercise} Question 4
:label: db-p2a-a2-q4
:nonumber:
How many mutations are described in OMIM and which types of mutations do they include?
:::

:::{solution} db-p2a-a2-q4
:class: dropdown
3 variants:

- .0001: deletion of exons 4–5.
- .0002: point mutation (transversion) T\>A.
- .0003: point mutation (transition) G\>A, which changes an amino acid (valine to methionine).

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 5
:label: db-p2a-a2-q5
:nonumber:
Which phenotype has been associated with the described variants?
:::

:::{solution} db-p2a-a2-q5
:class: dropdown
INSULIN-LIKE GROWTH FACTOR I DEFICIENCY

*Checked 2026-10-24, OMIM checked by hand.*
:::

Take a closer look at variant 147440.0003 — either the `.0003` row in the Table View, or the section headed `.0003 INSULIN-LIKE GROWTH FACTOR I DEFICIENCY` on the main entry page (<https://omim.org/entry/147440#0003>). Note the Table View shortens the number to `.0003`.

:::{exercise} Question 6
:label: db-p2a-a2-q6
:nonumber:
Answer the following questions:

a) Which change(s) in the protein are reported?

b) At which position in the protein is this change reported?

c) What is the rs number of this variant (also known as SNP)?

d) Which base is changed in the gene?

e) What is the consequence of this change?

f) How many literature references have described this variant? Describe in your own words what these references found on the influence of this particular variant on the protein.
:::

:::{solution} db-p2a-a2-q6
:class: dropdown
a) Valine to methionine.

b) Position 44 (V44M). OMIM numbers the *mature* IGF-1 peptide. dbSNP and ClinVar number the full precursor protein on the MANE transcript `NM_000618.5`, and there the same change is called p.Val92Met. Same variant, two numbering systems: always check which one a source uses.

c) rs121912430.

d) G\>A (on the coding strand; c.274G\>A).

e) The mutant IGF-1 binds the IGF-1 receptor about 90-fold less well, so it is effectively inactive: an inactivating mutation.

f) One paper: Walenkamp et al. (2005), <https://doi.org/10.1210/jc.2004-1254>. They produced the mutant protein and showed in receptor-binding assays that it binds the IGF-I receptor about 90 times less strongly. Although the patient had high levels of the mutant IGF-I in his blood, it contributed almost nothing to receptor binding, so his growth failure is explained by a lack of *bioactive* IGF-I.

*Checked 2026-10-24, OMIM checked by hand. Note for instructors: ClinVar's overall classification of this variant is now "conflicting" (checked 2026-10-23), not plainly pathogenic.*
:::

After looking at this gene and some variants from a disease perspective, we will now investigate the role of IGF1 in the hormonal control of pubertal growth spurt.

## Assignment 3: The biological context of IGF1 from WikiPathways

*Time: 30 min.*

The IGF-1 protein plays a vital role in development and growth of multiple tissues, including the growth plate in bones (a process called chondrogenesis). Look up the human “Hormonal control of pubertal growth spurt” pathway in WikiPathways (<https://www.wikipathways.org/pathways/WP4194.html>). This database (WikiPathways) shows you interactive drawings of pathway diagrams, which help to understand the biological context of genes, proteins and metabolites.

:::{exercise} Question 1
:label: db-p2a-a3-q1
:nonumber:
In which step(s) does the IGF-1 protein play a role according to this pathway?
:::

:::{solution} db-p2a-a3-q1
:class: dropdown
In response to GH (growth hormone, GH1), IGF1 has a stimulating effect on the growth plate in bone, both via the circulation and locally (autocrine/paracrine) within the growth plate.

```{figure} figures/2a-prep-wp4194.png
:name: db-fig-2a-prep-wp4194
:alt: WikiPathways WP4194, the two IGF1 nodes ringed.

WikiPathways WP4194, the two IGF1 nodes ringed. Figure from WikiPathways WP4194 (CC0).
```

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

:::{exercise} Question 2
:label: db-p2a-a3-q2
:nonumber:
Which other protein(s) (black boxes) or metabolites (blue boxes) have an (indirect) effect on the activity of IGF-1? Which protein(s) inhibit this step and what is the full name of the inhibitory protein?
:::

:::{solution} db-p2a-a3-q2
:class: dropdown
Proteins:

- GHRH (growth hormone–releasing hormone) has a positive effect on GH, which has a positive effect on IGF1.
- SST (somatostatin) has a negative effect on (inhibits) GH, and therefore negatively affects IGF1. Full name of the inhibitory protein: somatostatin.

Metabolites:

- Estrogens have a positive effect on GH, which has a positive effect on IGF1.

Look closely at the SST arrow: it is labelled "- effect", but drawn with the same open arrowhead as the stimulating arrows. Here the label carries the meaning; in a well-curated diagram the arrowhead itself would show inhibition (a T-bar). Diagrams are made by people, and a mismatch like this is worth reporting to the pathway's curators.

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

:::{exercise} Question 3
:label: db-p2a-a3-q3
:nonumber:
When was the last edit of this pathway?
:::

:::{solution} db-p2a-a3-q3
:class: dropdown
Read the date off the *last edited* badge on the pathway page. At the time of writing that was 30 November 2025.

⚠️ **Release-volatile** — WikiPathways is community-curated and this date moves with every edit. If the badge does not load, open *Share this pathway*: the citation text carries the date. Do not quote a date from a previous year's answer key.

```{figure} figures/2a-prep-wp4194-page.png
:name: db-fig-2a-prep-wp4194-page
:alt: WikiPathways WP4194, pathway page.

WikiPathways WP4194, pathway page. Figure from WikiPathways WP4194 (CC0).
```

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

Click the pathway diagram — this opens the interactive viewer in a new tab. Click the box labelled `IGF1` (not `IGF-1`); you will be redirected, via bioregistry.io, to the NCBI Gene entry. If that does not work, scroll to the Participants table on the pathway page and click the identifier next to IGF1.

:::{exercise} Question 4
:label: db-p2a-a3-q4
:nonumber:
What are the identifier, official symbol, and official full name of the IGF-1 gene?
:::

:::{solution} db-p2a-a3-q4
:class: dropdown
NCBI Gene ID: *3479*

Official symbol: *IGF1*

Official full name: *insulin like growth factor 1*

These can be found from the NCBI webpage that opens after clicking on IGF1. Besides the Entrez Gene ID (NCBI), the other identifiers are not linked directly from WikiPathways.

```{figure} figures/2a-prep-ncbi-igf1.png
:name: db-fig-2a-prep-ncbi-igf1
:alt: NCBI Gene 3479 (IGF1).

NCBI Gene 3479 (IGF1). Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

NCBI Gene ID:

Official symbol:

Official full name:

Even though there is much more to be had from this database, we now continue to one that describes genes and genomes themselves. That database is **Ensembl**, built at the European Bioinformatics Institute. You reach the human IGF1 gene from the link on the NCBI page, or directly at <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000017427>.

## Assignment 4: Genetic and functional information on IGF1 from Ensembl

*Time: 30 min.*

You will now study the IGF1 gene in more detail. For this we use **Ensembl**, a database of genes, genomes and their annotation, built at the European Bioinformatics Institute.

Ensembl rebuilt its website in 2026, and what you see is the new platform. Two things follow from that. Gene pages are shown in the app called the **Feature explorer**, so a gene has a URL of the form `www.ensembl.org/feature-explorer/<genome>/gene:<gene ID>`. And the numbers below come from a genome annotation that is updated regularly, so if what you see differs from the answer here, check the gene version shown on the page (the number after the dot, as in ENSG00000017427.19) before assuming you made a mistake: you may be looking at newer data than we were.

Open the human IGF1 gene: <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000017427>

:::{exercise} Question 1
:label: db-p2a-a4-q1
:nonumber:
What are other names of this gene, besides the official HGNC symbol IGF1?
:::

:::{solution} db-p2a-a4-q1
:class: dropdown
IGF, IGF-I, IGF1A, IGFI.

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 2
:label: db-p2a-a4-q2
:nonumber:
What is the chromosomal position (chromosome, location, and strand) of this gene?
:::

:::{solution} db-p2a-a4-q2
:class: dropdown
Chromosome 12: 102,395,874–102,481,857, reverse strand.

```{figure} figures/2a-prep-ens-igf1.png
:name: db-fig-2a-prep-ens-igf1
:alt: Ensembl, IGF1 gene page: location and strand in the header.

Ensembl, IGF1 gene page: location and strand in the header. Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19. Coordinates are given on assembly GRCh38 (GCA_000001405.29); a different assembly gives different numbers, which is why the assembly is part of the answer.*
:::

:::{exercise} Question 3
:label: db-p2a-a4-q3
:nonumber:
Switch to the **Transcripts table** view. How many transcripts (splice variants) are known for this gene? How many of them are protein coding?
:::

:::{solution} db-p2a-a4-q3
:class: dropdown
15 transcripts, of which 14 are protein coding. The fifteenth, ENST00000481539, is annotated `protein_coding_CDS_not_defined`: Ensembl believes it is transcribed but has not defined a coding sequence for it.

⚠️ **Release-volatile.** This count changes as the annotation is rebuilt: it was 11 transcripts in 2025, 7 when this manual was first revised on 31 August 2026, and 15 on 22 October 2026. Report the number you see together with the gene version and the date.

```{figure} figures/2a-prep-ens-igf1-tx.png
:name: db-fig-2a-prep-ens-igf1-tx
:alt: Ensembl, IGF1 Transcripts table (first rows; MANE Select ringed).

Ensembl, IGF1 Transcripts table (first rows; MANE Select ringed). Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 4
:label: db-p2a-a4-q4
:nonumber:
Which of the transcripts of this gene encodes the longest protein? Give its transcript ID and the protein length. Which transcript carries the flag **MANE Select**, and how long is its protein?
:::

:::{solution} db-p2a-a4-q4
:class: dropdown
Two transcripts tie for the longest protein, 195 amino acids: ENST00000307046.9 and ENST00001004634.1. The **MANE Select** transcript is ENST00000337514.11, which encodes 153 amino acids. MANE Select is the one reference transcript that Ensembl and NCBI agree on (it matches RefSeq `NM_000618.5`), chosen because it is well supported and biologically representative. That is why it is not necessarily the longest.

⚠️ **Release-volatile.** *Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 5
:label: db-p2a-a4-q5
:nonumber:
Compare your answer to question 3 with earlier counts for this gene: 11 transcripts in 2025 and 7 on 31 August 2026. The gene did not change; the annotation did. What does that tell you about quoting a transcript count in a report, and what should you write down alongside it?
:::

:::{solution} db-p2a-a4-q5
:class: dropdown
Nothing biological happened to IGF1. Ensembl updated its annotation and added new transcript models (you can recognise them by their recent, high ENST numbers). A transcript count is therefore a statement about a particular version of the annotation, not about the gene. Here the count doubled within two months while the website's release label ("2026-07") stayed the same, so the label alone is not enough.

In a report, quote the value **with the database, the version and the date you looked**: "15 transcripts (Ensembl, gene ENSG00000017427.19, accessed 22 October 2026)". This is the same reason papers cite database versions, and it is what makes a result reproducible by someone reading you a year later.
:::

:::{exercise} Question 6
:label: db-p2a-a4-q6
:nonumber:
Open **Gene relationships**, then **Homology**. Ensembl lists the IGF1 genes of other species (orthologues). How similar is the mouse IGF1 protein to the human one, and the zebrafish protein? Why does it matter for research on growth and ageing that IGF1 is so well conserved?
:::

:::{solution} db-p2a-a4-q6
:class: dropdown
Mouse Igf1: 92% protein similarity. Zebrafish igf1: 63%. Ensembl lists 31 orthologues in total, from primates to fish.

Because IGF1 (and the growth-hormone/IGF1 axis around it) is conserved, results from model organisms carry over to humans. Mice with reduced IGF1 signalling are smaller, and in several species, from worms to mice, reduced insulin/IGF1-like signalling also extends lifespan. Much of what is known about IGF1 in growth and ageing comes from such animal models (see also cases 5 and 7).

⚠️ **Release-volatile.** *Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*

```{figure} figures/2a-prep-ens-igf1-homology.png
:name: db-fig-2a-prep-ens-igf1-homology
:alt: Ensembl, IGF1 Gene relationships → Homology.

Ensembl, IGF1 Gene relationships → Homology. Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```
:::

## Check yourself

:::{note}
A practice quiz on this preparation will be added on the module page ({ref}`db-practice-quiz`).
:::
