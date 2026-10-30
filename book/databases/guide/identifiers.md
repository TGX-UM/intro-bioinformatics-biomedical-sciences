(db-guide-identifiers)=
# Identifier cheat-sheet

The table lists the identifiers you meet in the practicals. Examples are for IGF1 unless stated otherwise.

| Identifier | Database | Refers to | Example | What to know |
|---|---|---|---|---|
| Gene ID (a number) | NCBI Gene | gene | 3479 | Plain number, no prefix. Also called Entrez Gene ID |
| ENSG… | Ensembl | gene | ENSG00000017427.19 | ENS + G for gene; the human prefix has no species letters. Version after the dot |
| ENST… | Ensembl | transcript | ENST00000337514.11 | One gene has many ENSTs. Recently added models have high numbers, such as ENST00001004634 |
| ENSP… | Ensembl | protein | ENSP… | The protein product of one protein-coding ENST |
| HGNC:… and symbol | HGNC | official human gene symbol | HGNC:5464, IGF1 | The naming committee decides the official symbol; databases follow it |
| MIM number | OMIM | gene or phenotype entry | 147440 (gene), 608747 (disease) | Six digits. A prefix symbol tells you what kind of entry it is; see below |
| MIM number + .0001 | OMIM | allelic variant | 147440.0003 | A variant described in the OMIM gene entry |
| UniProt accession | UniProt | protein | P05019 | Six or ten characters. Isoforms get a suffix: P05019-1 is the canonical isoform, P05019-2 the next |
| UniProt entry name | UniProt | protein | IGF1_HUMAN | Readable, but can change; use the accession |
| NC_ | RefSeq | complete chromosome | NC_000012.12 | Chromosome 12, version 12 (GRCh38) |
| NG_ | RefSeq | genomic region of one gene (RefSeqGene) | NG_011713.1 | Exons, introns and flanking sequence |
| NM_ | RefSeq | curated mRNA | NM_000618.5 | Curated by NCBI staff |
| NR_ | RefSeq | curated non-coding RNA | NR_… | Transcribed but not translated |
| NP_ | RefSeq | curated protein | NP_000609.1 | Protein encoded by an NM_ |
| XM_, XR_, XP_ | RefSeq | predicted (model) mRNA, non-coding RNA, protein | XP_016874748.1 | Made by computational annotation, not yet curated. Treat with more caution |
| rs… | dbSNP | a variant position (reference SNP) | rs121912430 | One rs number can cover several alternative alleles at the same position |
| VCV… | ClinVar | one variant, all its classifications | VCV000014789 | The aggregate record for a variant |
| RCV… | ClinVar | one variant for one condition | RCV000015912 | Variant + condition combination |
| SCV… | ClinVar | one submission | SCV… | What one laboratory or group submitted |
| WP… | WikiPathways | pathway | WP3932 | Human, mouse and other species each have their own WP numbers |
| GO:… | Gene Ontology | biological process, molecular function or cellular component | GO:0048009 | Seven digits. Used for annotations in UniProt, Ensembl and NCBI |
| CHEBI:… | ChEBI | chemical entity or role | CHEBI:16469 (17β-estradiol) | Can also denote a class or a role, not just one molecule |
| CID | PubChem | one compound (unique structure) | 5757 (estradiol) | PubChem also has SIDs (deposited substances) and AIDs (assays) |
| HGVS | (notation, not a database) | a specific sequence change | NM_000618.5:c.274G>A | Always written together with its reference sequence; see below |

## OMIM prefixes

The symbol in front of a MIM number tells you what kind of entry it is:

| Prefix | Meaning |
|---|---|
| \* (asterisk) | a gene |
| \# (number sign) | a phenotype, usually a disease, whose molecular basis is known; the gene(s) are described in separate gene entries |
| \+ (plus) | an older type of entry that describes both a gene and a phenotype |
| % (percent) | a confirmed Mendelian phenotype or locus whose molecular basis is not yet known |
| no symbol | a phenotype for which a Mendelian basis is suspected but not clearly established |
| ^ (caret) | an entry that has been removed or moved to another entry |

So \*147440 is the IGF1 gene and \#608747 is insulin-like growth factor I deficiency.

## HGVS: describing a sequence change

The HGVS nomenclature (<https://hgvs-nomenclature.org/>) is the international standard for writing down variants. A description has two parts: a reference sequence, then a colon, then the change. The letter before the change says what kind of sequence the position is counted on:

| Prefix | Counted on | Example |
|---|---|---|
| g. | genomic sequence (a chromosome, or an NG_) | NC_000005.10:g.112828889C>T |
| c. | coding DNA of a transcript; position 1 is the A of the ATG start codon | NM_000038.6:c.1660C>T |
| n. | a non-coding transcript (no coding sequence to count from) | NR_…:n.… |
| p. | the protein | NP_000029.2:p.Arg554Ter, also written p.R554\* |

Some notation you will meet: `=` means "unchanged", so p.Gly608= is a synonymous change (literature often writes p.Gly608Gly). `Ter` or `*` is a stop codon. An intronic position is written relative to the nearest exon, as in c.373+5G>A (five bases into the intron after coding position 373).

Two things to watch:

- **Strand.** Genomic (g.) positions are given on the forward strand of the chromosome; c. positions on the transcript. For a gene on the reverse strand the bases are complementary: the IGF1 variant rs121912430 is C>T on the chromosome but c.274G>A on the transcript.
- **Which transcript.** The same genomic change can sit at a different c. and p. position in each transcript, because transcripts include different exons. The APC variant rs137854573 is codon 554 on NM_000038.6 but codon 536 on NM_001127511.3. A protein change without its reference sequence is ambiguous. That is why HGVS insists on writing the reference first, and why the MANE Select transcript is the default.

## The numbering trap: precursor versus mature protein

Many secreted proteins are made as a longer precursor, from which a signal peptide (and sometimes a propeptide) is cut off. Older literature, and OMIM, often number amino acids on the **mature** protein. dbSNP, ClinVar, Ensembl and current HGVS practice number them on the **full precursor** as encoded by the transcript. The same variant then has two names:

- **APOE ε4** (rs429358): Cys112Arg in the classic mature-protein numbering, p.Cys130Arg in dbSNP and ClinVar. The difference, 18, is the length of the APOE signal peptide.
- **IGF1** (rs121912430): Val44Met in OMIM, p.Val92Met in dbSNP. The difference, 48, is the IGF1 signal peptide (21 residues) plus propeptide (27 residues).

When two sources give different positions for what should be the same change, check the numbering system before you conclude they disagree.
