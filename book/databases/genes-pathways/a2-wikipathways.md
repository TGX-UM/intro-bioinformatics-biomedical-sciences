(db-p1-a2)=
# Assignment 2: The biological context of IGF1 from WikiPathways

*Time: 30 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

The IGF-1 protein plays a vital role in development and growth of multiple tissues, including the growth plate in bones (a process called chondrogenesis). Look up the human “Hormonal control of pubertal growth spurt” pathway in WikiPathways (<https://www.wikipathways.org/pathways/WP4194.html>). This database (WikiPathways) shows you interactive drawings of pathway diagrams, which help to understand the biological context of genes, proteins and metabolites.

:::{exercise} Question 1
:label: db-p1a2-q1
:nonumber:
In which step(s) does the IGF-1 protein play a role according to this pathway?
:::

:::{solution} db-p1a2-q1
:class: dropdown
In response to GH (growth hormone, GH1), IGF1 has a stimulating effect on the growth plate in bone, both via the circulation and locally (autocrine/paracrine) within the growth plate.

```{figure} ../figures/2a-prep-wp4194.png
:name: db-fig-2a-prep-wp4194
:alt: WikiPathways WP4194, the two IGF1 nodes ringed.

WikiPathways WP4194, the two IGF1 nodes ringed. Figure from WikiPathways WP4194 (CC0).
```

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

:::{exercise} Question 2
:label: db-p1a2-q2
:nonumber:
Which other protein(s) (black boxes) or metabolites (blue boxes) have an (indirect) effect on the activity of IGF-1? Which protein(s) inhibit this step and what is the full name of the inhibitory protein?
:::

:::{solution} db-p1a2-q2
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
:label: db-p1a2-q3
:nonumber:
When was the last edit of this pathway?
:::

:::{solution} db-p1a2-q3
:class: dropdown
Read the date off the *last edited* badge on the pathway page. At the time of writing that was 30 November 2025.

⚠️ **Release-volatile** — WikiPathways is community-curated and this date moves with every edit. If the badge does not load, open *Share this pathway*: the citation text carries the date. Do not quote a date from a previous year's answer key.

```{figure} ../figures/2a-prep-wp4194-page.png
:name: db-fig-2a-prep-wp4194-page
:alt: WikiPathways WP4194, pathway page.

WikiPathways WP4194, pathway page. Figure from WikiPathways WP4194 (CC0).
```

*Checked 2026-10-23, WikiPathways WP4194 (last edited 2025-11-30).*
:::

Click the pathway diagram — this opens the interactive viewer in a new tab. Click the box labelled `IGF1` (not `IGF-1`); you will be redirected, via bioregistry.io, to the NCBI Gene entry. If that does not work, scroll to the Participants table on the pathway page and click the identifier next to IGF1.

:::{exercise} Question 4
:label: db-p1a2-q4
:nonumber:
What are the identifier, official symbol, and official full name of the IGF-1 gene?
:::

:::{solution} db-p1a2-q4
:class: dropdown
NCBI Gene ID: *3479*

Official symbol: *IGF1*

Official full name: *insulin like growth factor 1*

These can be found from the NCBI webpage that opens after clicking on IGF1. Besides the Entrez Gene ID (NCBI), the other identifiers are not linked directly from WikiPathways.

```{figure} ../figures/2a-prep-ncbi-igf1.png
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
