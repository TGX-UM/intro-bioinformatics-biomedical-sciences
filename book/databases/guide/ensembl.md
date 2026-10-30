(db-guide-ensembl)=
# Ensembl

**What it is.** Ensembl, <https://www.ensembl.org/>, is a genome database run by the European Bioinformatics Institute (EMBL-EBI) near Cambridge, UK. It produces its own annotation of genes and transcripts on the genomes of humans and many other species, and integrates variants, comparative genomics (homologues) and regulatory data on top of it.

**What question it answers.** Where in the genome is this gene, on which strand, and what does its structure look like? Which transcripts does it have, and which of them code for protein? Which genes in other species are its orthologues? What does a given variant do to each transcript, and how common is it?

## The new Ensembl platform (2026)

In 2026 Ensembl replaced its website with a new platform. The old site's last release was Ensembl 116 (June 2026), and it remains available as an archive at <https://jun2026.archive.ensembl.org/>. The new site uses a different versioning system and release cycle, and it is organised as a set of separate apps:

- the **Feature explorer**, which shows gene and variant pages;
- the **Genome browser**, which shows a region of the genome graphically;
- **Tools**, including the Variant Effect Predictor (VEP);
- a **search** page, <https://www.ensembl.org/search>.

Addresses include the genome assembly. The current human assembly is GRCh38 (in full GRCh38.p14), which Ensembl identifies as GCA_000001405.29. A human gene page therefore has the form:

`https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000017427`

If you know the ENSG identifier you can type the address directly; otherwise use the search page and pick the human gene from the results.

## The gene page (Feature explorer)

The gene page opens with a summary: the gene symbol and full name, the stable identifier with its version (ENSG00000017427.19), the location (chromosome, start-end coordinates and strand) and the synonyms Ensembl knows. For IGF1 that is chromosome 12: 102,395,874-102,481,857, reverse strand, with synonyms IGF, IGF-I, IGF1A and IGFI.

The page has several views, which you switch between with the navigation on the page:

- **Transcripts**: a graphic of all transcripts of the gene, drawn along the genome, with exons as blocks joined by lines for the introns. This shows at a glance how transcripts differ in exon use and in where they start and end.
- **Transcripts table**: the same transcripts as a table, and the place to count and compare them. For each transcript you see its identifier (ENST with version), its **biotype**, the length of the transcript (in base pairs) and of the protein it encodes (in amino acids), and flags such as **MANE Select** and **Ensembl canonical**. You can reach this view directly by adding `?view=transcripts_table` to the gene address.
- **Gene function**: functional information about the gene product.
- **Gene relationships**, with **Homology**: the gene's orthologues (the same gene in other species). For each orthologue Ensembl gives the species, the gene symbol and identifier, the percentage protein similarity and coverage, and the type of hit. Mouse Igf1 is 92% similar to human IGF1; zebrafish igf1 63%. Watch for fish genes with an "a" or "b" suffix (mstnb for MSTN): fish have often kept two copies of genes after an ancient genome duplication.
- **External references**: the identifiers of the same gene in other databases, such as the OMIM gene and morbid (disease) numbers, NCBI Gene, HGNC, Expression Atlas and Reactome. Use these links to move between databases without retyping names.

**Biotypes** worth knowing: *protein_coding* (encodes a protein); *nonsense_mediated_decay* (has a premature stop codon, so the transcript is probably degraded before much protein is made); *retained_intron* (keeps an intron and is probably not translated); *protein_coding_CDS_not_defined* (Ensembl believes it belongs to a protein-coding gene but has not defined a coding sequence for it).

**Flags** worth knowing: *MANE Select* (see the first section); *Ensembl canonical* (Ensembl's own choice of one representative transcript per gene, which for most protein-coding genes is the MANE Select transcript); APPRIS and TSL (transcript support level), scores for how likely the transcript is to be the main isoform and how well it is supported by experimental evidence.

## The Genome browser

The Genome browser shows a region of a chromosome with tracks of features stacked below each other: genes and transcripts, variants, regulatory elements. Open it on a gene with:

`https://www.ensembl.org/genome-browser/GCA_000001405.29?focus=gene:ENSG00000017427`

A panel on the right lets you choose which tracks to show, grouped under Genomic, Variation and Regulation. You can zoom and drag to explore the neighbourhood of your gene.

## Variant pages

Search an rs number on the search page (for example `rs2229992`) and open the result in the Feature explorer. If the search box is greyed out, first open a human gene page (such as the IGF1 address above) or add Human GRCh38.p14 under *Find a genome*. A variant page has the form

`https://www.ensembl.org/feature-explorer/GCA_000001405.29/variant:5:112827157:rs2229992?allele=1`

The sidebar summarises the variant: its source (variants come from dbSNP, currently build 157), location, alleles, the **most severe consequence**, a CADD score and a VCF-style description. The main area shows **one alternative allele at a time**; you switch between the alleles on the page (the `allele=` part of the address changes with it). For the selected allele the page has these panels:

- **Transcript consequences**: what this allele does to each transcript of each overlapping gene, using standard consequence terms such as *synonymous_variant*, *missense_variant*, *stop_gained*, *splice_region_variant* or *intron_variant*, with the position in the coding sequence and the exon number. Look at the line for the MANE Select transcript first.
- **Regulatory consequences**: overlap with regulatory features such as promoters or enhancers.
- **Allele frequency**: how common the allele is in population studies, currently the **1000 Genomes Project** phase 3 (with five continental populations: African, American, East Asian, European, South Asian) and **gnomAD** v4.1, split into genomes and exomes. gnomAD is much larger. "Unknown" means the allele was not observed in these datasets, which for a rare variant is normal.
- **Genes**, **Variant phenotypes**, **Gene phenotypes** and **Citations** (the number of papers that mention the variant).

**CADD** (Combined Annotation Dependent Depletion) is a score for how deleterious a change is predicted to be, computed from many features such as conservation and consequence. Higher is more likely harmful; scores above 20 put a variant among the 1% most deleterious possible changes in the genome. It is a prediction, not evidence. In October 2026 the panel showed the same CADD value for every allele of a position, so read it as a statement about the position.

**The "most severe consequence" trap.** The header of a variant page shows the *most severe consequence across all alleles* at the position. For rs2229992 in APC it says **stop_gained**. Yet the common allele there (C, frequency 0.51 worldwide) is **synonymous**: it does not change the protein at all. The stop-gained consequence belongs to two other, rare alleles at the same base. Reading "stop_gained" off the header and concluding that half the world carries a truncated tumour suppressor would be badly wrong. Always select the specific allele you are interested in and read its own Transcript consequences.

**No clinical data.** The new Ensembl site shows **no clinical significance** for variants: Variant phenotypes is 0 even for well-known pathogenic APC alleles. For "is this allele harmful?", go to ClinVar, directly or through dbSNP.

## The Variant Effect Predictor (VEP)

VEP, at <https://www.ensembl.org/tools/vep>, predicts the consequences of variants you supply yourself (for example an rs number or an HGVS description) on all overlapping transcripts and regulatory features. It is the tool behind the consequences on the variant pages, and it is what you would use for a list of variants from a patient or an experiment. The old address `/vep` leads to the archived version.

## What moved to the archive

Some views of the old Ensembl site have no equivalent on the new platform yet. They are still available on the June 2026 archive, <https://jun2026.archive.ensembl.org/>, with data as of release 116:

- **phenotypes** linked to a gene or variant (including clinical significance taken from ClinVar);
- the **variant table** of a gene, listing all known variants in it with their consequences;
- **BioMart**, a tool for downloading tables of genes, identifiers and annotations in bulk, at <https://jun2026.archive.ensembl.org/biomart/martview>.

Archive data does not get updated. If you use it, say so, and quote "Ensembl release 116 (archive)".

## Pitfalls

- **Counts change under a fixed release label.** Quote the gene version and the date, not just "Release 2026-07" (see the first section).
- **Strand.** On a reverse-strand gene, the gene "starts" at the higher coordinate, and genomic alleles are the complement of the transcript bases.
- **Assembly.** Coordinates on GRCh37, the previous assembly still used in some older papers and clinical labs, are different numbers for the same position. Check which assembly a coordinate refers to.
- **Ensembl canonical is not always MANE Select**, and neither is necessarily the longest transcript.
- **Old tutorials describe the old site.** Videos and guides made before 2026 show pages that no longer exist.
