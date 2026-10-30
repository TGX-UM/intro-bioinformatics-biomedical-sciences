(db-p2-a3)=
# Assignment 3: One variant, two databases

*Time: 30 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

In this assignment, you will explore the dbSNP database using the variant rs2229992, which is located in the APC gene. dbSNP provides detailed information on genomic coordinates, allele changes, population frequencies, molecular consequences, clinical interpretation, and supporting studies. Go to dbSNP (<https://www.ncbi.nlm.nih.gov/snp/>) and search for rs2229992.

:::{exercise} Question 1
:label: db-p2a3-q1
:nonumber:
Which allelic **changes** and chromosomal position are reported for this SNP (GRCh38)? There is more than one alternative allele: list them all. How many publications are linked to this variant?
:::

:::{solution} db-p2a3-q1
:class: dropdown
Reference allele T, alternative alleles A, C and G, at chromosome 5, position 112,827,157 (GRCh38, `NC_000005.10`). The publication count is shown on the record and grows over time; dbSNP listed 20 citations on the day of checking (Ensembl lists 43).

⚠️ **Release-volatile** (publication count). *Checked 2026-10-28, dbSNP build 157.*

```{figure} ../figures/2b-train-dbsnp-summary.png
:name: db-fig-2b-train-dbsnp-summary
:alt: dbSNP rs2229992, summary.

dbSNP rs2229992, summary. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 2
:label: db-p2a3-q2
:nonumber:
Open the Variant Details tab. The location of the variant is represented by multiple prefixes (NC\_, NG\_, NM\_, NP\_). What does each prefix represent, and why are multiple sequence contexts shown?
:::

:::{solution} db-p2a3-q2
:class: dropdown
- NC\_ → chromosome-level RefSeq genomic sequence.
- NG\_ → RefSeqGene record: a curated genomic region covering the gene, including exons, introns and flanking sequence.
- NM\_ → RefSeq mRNA (transcript) sequence.
- NP\_ → RefSeq protein sequence.

Multiple contexts are shown because the same variant must be placed on the genome, the gene, the transcript(s) and the protein. This keeps its position consistent across all kinds of sequence.

```{figure} ../figures/2b-train-dbsnp-details.png
:name: db-fig-2b-train-dbsnp-details
:alt: dbSNP rs2229992, Variant Details.

dbSNP rs2229992, Variant Details. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 3
:label: db-p2a3-q3
:nonumber:
Go to Clinical Significance. Which diseases or phenotypes are associated with this SNP? Which allele appears to have the strongest harmful effect?
:::

:::{solution} db-p2a3-q3
:class: dropdown
The phenotype reported is familial adenomatous polyposis 1 (FAP1). The T→C allele is classified **benign**, by an expert panel. The T→G allele, a stop-gained change (p.Tyr486Ter), is classified **pathogenic**, from a single submitter. So T→G is the allele with the strongest harmful interpretation. The T→A allele would also create a stop codon, but has no ClinVar record.

⚠️ **Release-volatile** — ClinVar classifications are revised as evidence accumulates. *Checked 2026-10-23, ClinVar.*

```{figure} ../figures/2b-train-dbsnp-clinical.png
:name: db-fig-2b-train-dbsnp-clinical
:alt: dbSNP rs2229992, Clinical Significance.

dbSNP rs2229992, Clinical Significance. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 4
:label: db-p2a3-q4
:nonumber:
What is the clinical interpretation? How can the same genomic position have alleles with different clinical impacts?
:::

:::{solution} db-p2a3-q4
:class: dropdown
Clinical interpretations range from benign (T→C) to pathogenic (T→G). Different alleles at the same position change the codon in different ways. Here T→C keeps tyrosine (TAT→TAC, synonymous), while T→G and T→A turn it into a stop codon (TAG or TAA). Each substitution can therefore have its own molecular and clinical effect, even at the same genomic location.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5
:label: db-p2a3-q5
:nonumber:
Go to the Frequency tab. What is the global allele frequency in the 1000 Genomes study (use the `1000Genomes` row with n=5008, not `1000Genomes_30X`)?
:::

:::{solution} db-p2a3-q5
:class: dropdown
T = 0.4900, C = 0.5100. The alternative allele C is slightly *more* common worldwide than the reference allele T. The reference genome is one particular sequence, not a record of the most common allele.

```{figure} ../figures/2b-train-dbsnp-frequency.png
:name: db-fig-2b-train-dbsnp-frequency
:alt: dbSNP rs2229992, Frequency tab (1000Genomes ringed).

dbSNP rs2229992, Frequency tab (1000Genomes ringed). Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 6
:label: db-p2a3-q6
:nonumber:
Which continental populations are represented in the 1000 Genomes dataset?
:::

:::{solution} db-p2a3-q6
:class: dropdown
African, American (admixed American), East Asian, European and South Asian.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 7
:label: db-p2a3-q7
:nonumber:
According to 1000 Genomes, which continental population has the lowest frequency of the alternative allele?
:::

:::{solution} db-p2a3-q7
:class: dropdown
The African population: reference allele T at 0.838 and alternative allele C at 0.162.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 8
:label: db-p2a3-q8
:nonumber:
For the African and American populations, calculate Hardy–Weinberg genotype frequencies (Z/Z, Z/z, z/z), taking Z = the reference allele T and z = the alternative allele C. How do the expected genotype frequencies differ between the two populations?
:::

:::{solution} db-p2a3-q8
:class: dropdown
The Hardy–Weinberg principle says that, under equilibrium, genotype frequencies follow from allele frequencies: p² + 2pq + q² = 1. More information: <https://en.wikipedia.org/wiki/Hardy%E2%80%93Weinberg_principle>

African (p = T = 0.838, q = C = 0.162):

- Z/Z = T/T = p² = 0.838² = 0.702
- Z/z = T/C = 2pq = 2 × 0.838 × 0.162 = 0.272
- z/z = C/C = q² = 0.162² = 0.026

American (p = T = 0.333, q = C = 0.667):

- Z/Z = T/T = p² = 0.333² = 0.111
- Z/z = T/C = 2pq = 2 × 0.333 × 0.667 = 0.444
- z/z = C/C = q² = 0.667² = 0.445

Interpretation: in the African population the C/C homozygote is rare because the C allele is uncommon. In the American population almost half of people are expected to be C/C, reflecting the much higher frequency of C.

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 9
:label: db-p2a3-q9
:nonumber:
dbSNP reports **stop-gained** among the molecular consequences at this position in APC, a tumour-suppressor gene. Yet you have just seen alternative-allele frequencies above 0.65 in some populations, and 0.51 globally. Those two facts do not sit together comfortably. Look again at which allele carries which consequence, and explain the apparent contradiction. What does this tell you about reading a single "most severe consequence" label off a variant record?
:::

:::{solution} db-p2a3-q9
:class: dropdown
The contradiction is only apparent, because the consequences belong to *different alleles* at the same position. The allele that is common, reaching high frequency in some populations, is the synonymous change, which leaves the protein sequence untouched. The stop-gained alleles are separate, rare alternatives at the same base.

A "most severe consequence" summary reports the worst consequence seen at the position, across all alleles. That is deliberately conservative, and it is not a statement about the allele most people carry. Read "stop-gained" and stop there, and you would conclude that most people in some populations carry a truncated APC. That is impossible for a tumour suppressor whose loss causes familial adenomatous polyposis.

The general lesson: a variant record describes a *position*, and a position can carry several alleles with different consequences and different clinical interpretations. Always resolve which allele you are talking about before quoting a consequence or a pathogenicity call.

⚠️ **Release-volatile** — allele frequencies are re-computed as population datasets grow. *Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 10
:label: db-p2a3-q10
:nonumber:
Now open the same variant in **Ensembl**. Type `rs2229992` into the search box at <https://www.ensembl.org/search> (if the box is greyed out, first add Human GRCh38.p14 under **Find a genome**) and open the result in the Feature explorer. Ensembl's variant page shows one alternative allele at a time: select the **C** allele, then open **Allele frequency**.

a) Does Ensembl's 1000 Genomes frequency for the C allele agree with dbSNP? Which other dataset does Ensembl show?

b) What does Ensembl say in the header bar as "Most severe consequence"? Open **Transcript consequences** for the C allele: what is the consequence on the MANE Select transcript?

c) Ensembl shows no clinical significance for this variant (Variant phenotypes: 0). Where did you find that information instead? What does that tell you about which database to use for which question?
:::

:::{solution} db-p2a3-q10
:class: dropdown
a) Yes. Ensembl shows 1000 Genomes phase 3 with global 0.51 for C, and per population African 0.162, American 0.667, East Asian 0.665, European 0.580, South Asian 0.638, the same as dbSNP. It also shows gnomAD v4.1 (genomes 0.482, exomes 0.587), a much larger dataset.

b) The header says **stop_gained**, exactly the trap from question 9. The header summarises the position across all alleles; the C allele itself is a **synonymous variant** on the MANE Select transcript ENST00000257430.

c) In dbSNP, which takes it from ClinVar. Ensembl's rebuilt website gives consequences and frequencies but, unlike its old site, no clinical interpretations. Use Ensembl or dbSNP for *what a variant does to the transcript and how common it is*, and ClinVar (directly or through dbSNP) for *what it means clinically*.

⚠️ **Release-volatile.** *Checked 2026-10-22, Ensembl (Release 2026-07; variant data from dbSNP 157).*

```{figure} ../figures/2b-train-ens-var-freq.png
:name: db-fig-2b-train-ens-var-freq
:alt: Ensembl, rs2229992: header and allele frequencies.

Ensembl, rs2229992: header and allele frequencies. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```
:::
