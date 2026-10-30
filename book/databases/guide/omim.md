(db-guide-omim)=
# OMIM

**What it is.** OMIM, *Online Mendelian Inheritance in Man*, <https://omim.org/>, is a catalogue of human genes and genetic phenotypes, with a focus on Mendelian disorders. It is written and curated by experts at Johns Hopkins University, who summarise the published literature in readable text entries. It started as a printed book by Victor McKusick in the 1960s.

**What question it answers.** Which diseases are linked to this gene, and with what inheritance pattern? What is known about this genetic disease, and which genes cause it? Which variants in this gene were described in the literature, and what did those papers find?

**Getting there.** Type a gene symbol, a disease name or a MIM number in the search box on the home page. The gene entry for IGF1 is <https://omim.org/entry/147440>. NCBI Gene and Ensembl both link to OMIM from the gene page.

**Note on access.** OMIM checks that visitors are human, so you may be asked to pass a short browser check. OMIM's content is copyrighted and may not be reproduced: in this course we link to it but never copy or screenshot it.

## Reading a gene entry

A gene entry has a title (the gene name and symbol, with its MIM number and prefix), alternative titles and symbols, the gene's cytogenetic and genomic location, and then a **Gene-Phenotype Relationships** table. That table lists every phenotype linked to the gene, with its location, the phenotype name, the **Phenotype MIM number**, the **inheritance** (for example AR for autosomal recessive, AD for autosomal dominant) and the **phenotype mapping key**.

The phenotype mapping key is a number from 1 to 4. A **3** means the molecular basis of the disorder is known: a causative mutation has been found in this gene. Lower numbers mean the disorder was only mapped to this region. Symbols in the phenotype name carry meaning too: a phenotype in braces, `{ }`, is a susceptibility to a multifactorial disorder (such as severe coronary artery disease for APOE), and a question mark means the gene-phenotype link is provisional. Treat a braces entry very differently from a Mendelian disease: carrying the allele raises risk, it does not cause the disease on its own.

Below the table follows the text of the entry, under headings such as Description, Cloning and Expression, Gene Function, Molecular Genetics and Animal Model, each with numbered literature references. The navigation on the left of the page jumps to each section. The entry ends with the **References** and an **Edit History**, from which you can read when the entry was last changed.

## Allelic variants

Near the end of a gene entry, the **Allelic Variants** section describes a selection of variants, each numbered after the gene's MIM number: 147440.0001, .0002, .0003. These are not all known variants, but examples chosen by the curators because they were reported in the literature as disease-relevant. Each variant has a short text with the amino-acid change, the phenotype, the dbSNP rs number and ClinVar link where available, and the references. A **Table View** (link next to the section heading, or <https://omim.org/allelicVariants/147440>) lists them compactly. In the table, variant numbers are shortened to `.0003`.

## Pitfalls

- **Old numbering.** OMIM often uses the amino-acid numbering of the original paper, which may be the mature protein (see the numbering trap above). The IGF1 variant OMIM calls V44M is p.Val92Met in dbSNP.
- **Selection, not completeness.** The allelic variants are a curated selection. For all known variants in a gene and their current clinical classification, use ClinVar.
- **Interpretation dates.** The text reflects the literature at the time of writing. A variant OMIM described as disease-causing in 2005 may since have been reclassified in ClinVar (the IGF1 V44M variant is now "conflicting" there).
- **OMIM content via NCBI.** NCBI pages show OMIM numbers and titles, but they are still OMIM's content, with OMIM's copyright.
