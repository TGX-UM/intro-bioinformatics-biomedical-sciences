(db-guide-ncbi-gene)=
# NCBI Gene

**What it is.** NCBI Gene, <https://www.ncbi.nlm.nih.gov/gene/>, is the gene database of the US National Center for Biotechnology Information (NCBI), part of the National Library of Medicine. NCBI also hosts PubMed, dbSNP, ClinVar, RefSeq and PubChem, and NCBI Gene connects them. It is a classic aggregating resource: one page per gene, for many species, pulling together nomenclature, genomic location, reference sequences, expression, phenotypes, pathways, variation, literature and links.

**What question it answers.** A broad first overview of a gene: what it is called, where it is, which reference sequences exist for it, where it is expressed, which phenotypes and pathways it is linked to, and where to go next.

**Getting there.** Search by symbol on the NCBI Gene page and choose the entry for *Homo sapiens* (the result list includes other species), or go directly by Gene ID: <https://www.ncbi.nlm.nih.gov/gene/3479>. WikiPathways and Ensembl link to it.

## Sections of the gene page

The page is long. A **table of contents** on the right lets you jump to each section. NCBI is also building a new version of this page (links such as **Try the new Gene page** appear near the top); this guide describes the classic page that opens by default. The sections you use in the practicals:

- **Summary**: the Gene ID, official symbol and full name (both "provided by HGNC"), links to the same gene in Ensembl and OMIM, the gene type, the organism, **Also known as** (the aliases), and, for many genes, a short written summary of its function, usually provided by RefSeq curators. A one-line expression summary follows.
- **Genomic context**: the cytogenetic location (12q23.2 for IGF1), the **Exon count** (counted over all transcripts together), and a table with the exact coordinates on each assembly: GRCh38 (NC_000012.12), the newer telomere-to-telomere assembly T2T-CHM13, and the previous assembly GRCh37. "complement" after the coordinates means the gene lies on the reverse strand.
- **Expression**: a bar chart of RNA levels across tissues. A drop-down at the top of the section chooses the dataset. In October 2026 it offered three: a **fetal** tissue dataset (*Tissue-specific circular RNA induction during human fetal development*, six organs between 10 and 20 weeks of gestation), *RNA sequencing of total RNA from 20 human tissues*, and **HPA RNA-seq normal tissues** (from the Human Protein Atlas: 27 adult normal tissues; the chart plots TPM). The section opens on the fetal dataset, so for adult tissues you have to switch.
- **Phenotypes**: under *Associated conditions*, the diseases linked to the gene, each with links to MedGen and OMIM; also genome-wide association studies (GWAS Catalog) and links to genetic tests.
- **Variation**: links to the gene's variants in ClinVar and other variation resources.
- **Pathways from PubChem**: an embedded panel listing pathways from Reactome, WikiPathways, PANTHER and other sources that include the gene. It has its own search box; type `WP` and a number to find a WikiPathways pathway.
- **Interactions**: protein interaction partners from BioGRID and other sources.
- **General gene information**: orthologues (under Homology) and the **Gene Ontology** annotations, with an evidence code for each (see the UniProt section for what the codes mean).
- **NCBI Reference Sequences (RefSeq)**: the reference sequences for the gene; see below.

## The RefSeq section

This section has two parts.

The first, *RefSeqs maintained independently of Annotated Genomes*, holds the curated records: the genomic region (NG_, labelled RefSeqGene), and then each transcript with its protein, as NM_ → NP_ pairs (plus NR_ for curated non-coding RNAs). Each pair has a status (REVIEWED is the best-curated level), a description of how this transcript variant differs from the others, and, under *Related*, the matching Ensembl ENSP and ENST identifiers. Each protein has a name, such as "insulin-like growth factor 1 isoform 4 preproprotein", which tells you which isoform it is and that it is made as a precursor. On this classic page the MANE Select transcript is not marked as such, but it is listed first (for IGF1, NM_000618.5); dbSNP, ClinVar and Ensembl do label it.

The second part, *RefSeqs of Annotated Genomes*, holds the records that belong to a specific genome build: the chromosome (NC_) and the predicted XM_ → XP_ models. It is split per assembly, and the same predicted models are listed once for GRCh38 and again for T2T-CHM13. For IGF1 that is 3 predicted models on GRCh38 and 3 on T2T, with different accessions.

**Counting traps.** Say exactly what you counted. "13 RefSeq transcripts for IGF1" counts the 7 curated NM_ records plus all 6 XM_ entries, but those 6 are 3 models listed for two assemblies; on GRCh38 alone there are 7 curated and 3 predicted. And at the top of the RefSeq section there is a link **Try the new Transcript table**. It leaves NCBI Gene for the **NCBI Datasets** website (<https://www.ncbi.nlm.nih.gov/datasets/>), which shows the gene's transcripts in a newer table and counts them differently again. Each count is defensible; just say which page and which rule you used.

## Pitfalls

- **Check the species.** A search for "IGF1" returns the gene in dozens of organisms.
- **Check which expression dataset you are looking at.** The fetal dataset opens by default.
- **Expression shows only what was sampled.** The HPA dataset has no skeletal-muscle or cartilage samples, so MSTN (a muscle gene) shows only trace values and FGFR3 is missing from the growth plate where it matters. No signal is not the same as no expression.
- **Predicted models change.** The number of XM_ records shifts with every annotation release (the RefSeq annotation in October 2026 was RS_2025_08).
- **Aliases differ from Ensembl's.** NCBI lists MGF as an alias of IGF1; Ensembl lists IGF1A. Neither list is complete.
- **Phenotypes are aggregated.** Follow the link to the source (OMIM, ClinVar) for details and dates.
