(db-guide-dbsnp-clinvar)=
# dbSNP and ClinVar

Two NCBI databases work together for variants. **dbSNP**, <https://www.ncbi.nlm.nih.gov/snp/>, catalogues short genetic variants (single-nucleotide variants, small insertions and deletions) and gives each position a reference SNP identifier, the **rs number**. **ClinVar**, <https://www.ncbi.nlm.nih.gov/clinvar/>, collects **clinical interpretations** of variants, submitted by diagnostic laboratories, research groups and expert panels. A dbSNP page shows the ClinVar interpretations for its alleles, but ClinVar is the primary source.

**What question they answer.** Where exactly is this variant, which alleles exist there, and what does each do to the transcripts and protein? How common is each allele in different populations? Is an allele considered pathogenic, benign or uncertain, by whom and on what evidence?

## A dbSNP record

Open a record by its rs number, for example <https://www.ncbi.nlm.nih.gov/snp/rs2229992>. The header shows the current build (build 157, released in September 2024 and still current in October 2026), organism, **position** (chromosome and coordinate on GRCh38.p14), **alleles** (the reference allele, then all alternative alleles, such as `T>A / T>C / T>G`), variation type, a short frequency summary, the clinical significance, the gene and consequence, and the number of publications. Below are tabs:

- **Variant Details**: the variant placed on every relevant sequence: the chromosome (NC_), the gene region (NG_), each transcript (NM_, with the c. position and codon change) and each protein (NP_, with the amino-acid change), for each allele. Use the line for the MANE Select transcript. This is where you see that one genomic change gets different protein positions in different transcripts.
- **Clinical Significance**: the ClinVar records for the variant, **one row per allele and condition**, with the RCV accession, the allele, the condition and the classification. Follow the RCV link to ClinVar for the full story.
- **Frequency**: allele frequencies in many population studies. For the **1000 Genomes Project**, use the row labelled `1000Genomes` with a sample size of n = 5008 alleles (2504 people), not `1000Genomes_30X`, which is a later re-sequencing. Expand it for the five continental populations: African (AFR), admixed American (AMR), East Asian (EAS), European (EUR) and South Asian (SAS). Other rows include gnomAD, ALFA (NCBI's own aggregate), TOPMed and national cohorts.
- **HGVS Expressions**, **Submissions**, **History**, **Publications** and **Flanks** (the surrounding sequence).

## Reading frequencies

A frequency is given per allele, as in "C = 0.5100". Reference and alternative frequencies at a biallelic position add up to 1. Two things trip students up:

- The **reference allele is not necessarily the common one**. The reference genome is one particular sequence. At rs2229992 the reference allele T has a global frequency of 0.49, so the alternative allele C is the more common one.
- The header summary shows, for each study, **whichever allele that study reports**, often the minor one, so one line says "T = 0.41" and the next "C = 0.48". Compare like with like by checking which allele each number belongs to.

With an allele frequency you can estimate genotype frequencies under Hardy-Weinberg equilibrium: with allele frequencies p and q, the expected genotype frequencies are p², 2pq and q².

## ClinVar classifications and review stars

A ClinVar classification uses a standard scale: **pathogenic**, **likely pathogenic**, **uncertain significance** (VUS), **likely benign**, **benign**, plus other categories such as **risk factor**, **drug response** and **conflicting classifications of pathogenicity** (when submitters disagree).

Each record has a **review status**, shown as gold stars, which tells you how much to trust the classification:

| Stars | Review status |
|---|---|
| none | no assertion criteria provided (a submitter gave a classification without saying on what basis) |
| one | criteria provided, single submitter; or criteria provided, conflicting classifications |
| two | criteria provided, multiple submitters, no conflicts |
| three | reviewed by expert panel |
| four | practice guideline |

A "pathogenic" with no stars from 2005 and a "pathogenic" from an expert panel are very different statements. See <https://www.ncbi.nlm.nih.gov/clinvar/docs/review_status/>.

ClinVar's own record for a variant (VCV) shows the aggregate classification at the top, then the list of submissions (SCV) with who submitted them, when, for which condition, and the evidence they give. Following a classification through to its submitters is how you judge it.

## Multi-allelic positions: always say which allele

Many rs numbers cover more than one alternative allele, and the alleles can have completely different effects. At rs137854573 in APC, the reference C can change to:

| Allele | Effect on NM_000038.6 | ClinVar |
|---|---|---|
| C>T | p.Arg554Ter, stop gained | pathogenic (familial adenomatous polyposis) |
| C>G | p.Arg554Gly, missense | no record |
| C>A | p.Arg554=, synonymous | likely benign |

"rs137854573 is pathogenic" is therefore not a meaningful statement. "rs137854573 C>T (p.Arg554Ter) is pathogenic for FAP" is. The same reasoning lies behind the most-severe-consequence trap described under Ensembl.

## Pitfalls

- **dbSNP lags ClinVar.** The ClinVar rows on a dbSNP page come from the dbSNP build, which can be well over a year old. A variant listed as "pathogenic" in dbSNP can be "conflicting" in ClinVar today (the IGF1 V44M variant is an example). For the current classification, open ClinVar.
- **Rare variants often have no frequency** in 1000 Genomes, which sampled only 2504 people. Look at gnomAD, which is far larger.
- **A synonymous variant can still cause disease.** LMNA c.1824C>T (p.Gly608=) changes no amino acid but activates a hidden splice site, causing Hutchinson-Gilford progeria. The consequence term describes the codon, not what happens to splicing.
- **Risk alleles look different.** APOE ε4 (rs429358) is common (15% of alleles worldwide in 1000 Genomes) and is classified as a risk factor, not as pathogenic. A strong disease-causing allele stays rare; a modest risk allele acting late in life can become common.
