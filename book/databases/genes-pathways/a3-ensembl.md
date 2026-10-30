(db-p1-a3)=
# Assignment 3: Genetic and functional information on IGF1 from Ensembl

*Time: 30 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

You will now study the IGF1 gene in more detail. For this we use **Ensembl**, a database of genes, genomes and their annotation, built at the European Bioinformatics Institute.

Ensembl rebuilt its website in 2026, and what you see is the new platform. Two things follow from that. Gene pages are shown in the app called the **Feature explorer**, so a gene has a URL of the form `www.ensembl.org/feature-explorer/<genome>/gene:<gene ID>`. And the numbers below come from a genome annotation that is updated regularly, so if what you see differs from the answer here, check the gene version shown on the page (the number after the dot, as in ENSG00000017427.19) before assuming you made a mistake: you may be looking at newer data than we were.

Open the human IGF1 gene: <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000017427>

:::{exercise} Question 1
:label: db-p1a3-q1
:nonumber:
What are other names of this gene, besides the official HGNC symbol IGF1?
:::

:::{solution} db-p1a3-q1
:class: dropdown
IGF, IGF-I, IGF1A, IGFI.

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 2
:label: db-p1a3-q2
:nonumber:
What is the chromosomal position (chromosome, location, and strand) of this gene?
:::

:::{solution} db-p1a3-q2
:class: dropdown
Chromosome 12: 102,395,874–102,481,857, reverse strand.

```{figure} ../figures/2a-prep-ens-igf1.png
:name: db-fig-2a-prep-ens-igf1
:alt: Ensembl, IGF1 gene page: location and strand in the header.

Ensembl, IGF1 gene page: location and strand in the header. Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19. Coordinates are given on assembly GRCh38 (GCA_000001405.29); a different assembly gives different numbers, which is why the assembly is part of the answer.*
:::

:::{exercise} Question 3
:label: db-p1a3-q3
:nonumber:
Switch to the **Transcripts table** view. How many transcripts (splice variants) are known for this gene? How many of them are protein coding?
:::

:::{solution} db-p1a3-q3
:class: dropdown
15 transcripts, of which 14 are protein coding. The fifteenth, ENST00000481539, is annotated `protein_coding_CDS_not_defined`: Ensembl believes it is transcribed but has not defined a coding sequence for it.

⚠️ **Release-volatile.** This count changes as the annotation is rebuilt: it was 11 transcripts in 2025, 7 when this manual was first revised on 31 August 2026, and 15 on 22 October 2026. Report the number you see together with the gene version and the date.

```{figure} ../figures/2a-prep-ens-igf1-tx.png
:name: db-fig-2a-prep-ens-igf1-tx
:alt: Ensembl, IGF1 Transcripts table (first rows; MANE Select ringed).

Ensembl, IGF1 Transcripts table (first rows; MANE Select ringed). Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 4
:label: db-p1a3-q4
:nonumber:
Which of the transcripts of this gene encodes the longest protein? Give its transcript ID and the protein length. Which transcript carries the flag **MANE Select**, and how long is its protein?
:::

:::{solution} db-p1a3-q4
:class: dropdown
Two transcripts tie for the longest protein, 195 amino acids: ENST00000307046.9 and ENST00001004634.1. The **MANE Select** transcript is ENST00000337514.11, which encodes 153 amino acids. MANE Select is the one reference transcript that Ensembl and NCBI agree on (it matches RefSeq `NM_000618.5`), chosen because it is well supported and biologically representative. That is why it is not necessarily the longest.

⚠️ **Release-volatile.** *Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*
:::

:::{exercise} Question 5
:label: db-p1a3-q5
:nonumber:
Compare your answer to question 3 with earlier counts for this gene: 11 transcripts in 2025 and 7 on 31 August 2026. The gene did not change; the annotation did. What does that tell you about quoting a transcript count in a report, and what should you write down alongside it?
:::

:::{solution} db-p1a3-q5
:class: dropdown
Nothing biological happened to IGF1. Ensembl updated its annotation and added new transcript models (you can recognise them by their recent, high ENST numbers). A transcript count is therefore a statement about a particular version of the annotation, not about the gene. Here the count doubled within two months while the website's release label ("2026-07") stayed the same, so the label alone is not enough.

In a report, quote the value **with the database, the version and the date you looked**: "15 transcripts (Ensembl, gene ENSG00000017427.19, accessed 22 October 2026)". This is the same reason papers cite database versions, and it is what makes a result reproducible by someone reading you a year later.
:::

:::{exercise} Question 6
:label: db-p1a3-q6
:nonumber:
Open **Gene relationships**, then **Homology**. Ensembl lists the IGF1 genes of other species (orthologues). How similar is the mouse IGF1 protein to the human one, and the zebrafish protein? Why does it matter for research on growth and ageing that IGF1 is so well conserved?
:::

:::{solution} db-p1a3-q6
:class: dropdown
Mouse Igf1: 92% protein similarity. Zebrafish igf1: 63%. Ensembl lists 31 orthologues in total, from primates to fish.

Because IGF1 (and the growth-hormone/IGF1 axis around it) is conserved, results from model organisms carry over to humans. Mice with reduced IGF1 signalling are smaller, and in several species, from worms to mice, reduced insulin/IGF1-like signalling also extends lifespan. Much of what is known about IGF1 in growth and ageing comes from such animal models (see also cases 5 and 7).

⚠️ **Release-volatile.** *Checked 2026-10-23, Ensembl gene ENSG00000017427.19.*

```{figure} ../figures/2a-prep-ens-igf1-homology.png
:name: db-fig-2a-prep-ens-igf1-homology
:alt: Ensembl, IGF1 Gene relationships → Homology.

Ensembl, IGF1 Gene relationships → Homology. Screenshot of Ensembl, 2026-10-24 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```
:::
