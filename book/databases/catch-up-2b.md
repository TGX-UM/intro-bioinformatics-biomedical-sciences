(db-catch-up-2b)=
# Extra practice: catch-up assignment 2B

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

BBS2002 students who missed the 2B computer session do this assignment instead. For everyone
else it is extra practice with the databases of practical 2B, on a new example. It does not
replace the original assignments and does not cover all their content.

The VHL gene is associated with kidney tumours and named after von Hippel-Lindau syndrome,
which it can cause. You study the gene, the function of the protein it encodes, known genetic
variations and mutations in the gene, and their effect on the function and structure of the
protein.

*Background: the [Reference guide](guide/index.md) has one page per database.*

## Assignment 1: The VHL gene and the variant rs5030809

Ensembl rebuilt its website in 2026. The new site no longer shows the clinical interpretation of variants or the gene-wide variant table this assignment used, so it uses Ensembl for the gene and dbSNP for the variant. Knowing which database holds which kind of information is itself part of the point.

### Part A: the VHL gene in Ensembl

Open <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000134086>

:::{exercise} Question 1
:label: db-c2b-a1-q1
:nonumber:
What is the chromosomal location and strand of VHL, and on which genome assembly are those coordinates given?
:::

:::{solution} db-c2b-a1-q1
:class: dropdown
Chromosome 3: 10,141,764–10,153,676, forward strand, on GRCh38 (GCA_000001405.29).

```{figure} figures/cu2b-ens-vhl.png
:name: db-fig-cu2b-ens-vhl
:alt: Ensembl, VHL gene page.

Ensembl, VHL gene page. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134086.12.*
:::

:::{exercise} Question 2
:label: db-c2b-a1-q2
:nonumber:
Switch to the **Transcripts table** view. How many transcripts does VHL have, and how many are protein coding? Which transcript is MANE Select, and how long is its protein? How long is the longest protein?
:::

:::{solution} db-c2b-a1-q2
:class: dropdown
15 transcripts, of which 10 are protein coding. The MANE Select transcript is ENST00000256474.3 (matching RefSeq `NM_000551.4`), encoding 213 amino acids. The longest protein, 250 amino acids, comes from ENST00000696153.3. The MANE Select protein is not the longest one: the reference transcript is chosen for being well supported, not for its length.

⚠️ **Release-volatile** — Ensembl reported 6 transcripts on 31 August 2026 and 15 on 22 October, under the same release label. Report the count with the gene version shown on the page and the date.

```{figure} figures/cu2b-ens-vhl-tx.png
:name: db-fig-cu2b-ens-vhl-tx
:alt: Ensembl, VHL Transcripts table (MANE Select ringed).

Ensembl, VHL Transcripts table (MANE Select ringed). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000134086.12.*
:::

:::{exercise} Question 3
:label: db-c2b-a1-q3
:nonumber:
Switch to the **Genome browser** app (the "View in" button on the gene page). Which other genes lie in the same region (zoom out)? Name five gene symbols.
:::

:::{solution} db-c2b-a1-q3
:class: dropdown
Any five neighbouring genes on chromosome 3p25 read off the browser track are acceptable. The point of the question is that genes are not evenly spaced and that a variant's neighbourhood is visible at a glance — not the specific list, which depends on how far you zoom out. Say how wide a window you used.
:::

### Part B: the variant rs5030809 in dbSNP

Open <https://www.ncbi.nlm.nih.gov/snp/rs5030809>

:::{exercise} Question 4
:label: db-c2b-a1-q4
:nonumber:
What is the chromosomal position of this variant on GRCh38, and which reference and alternative alleles are reported?
:::

:::{solution} db-c2b-a1-q4
:class: dropdown
Chromosome 3, position 10,142,139 on GRCh38 (`NC_000003.12`). The reference allele is T, with alternative alleles A and C.

```{figure} figures/cu2b-dbsnp-summary.png
:name: db-fig-cu2b-dbsnp-summary
:alt: dbSNP rs5030809, summary.

dbSNP rs5030809, summary. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 5
:label: db-c2b-a1-q5
:nonumber:
Open the **Variant Details** tab. For transcript `NM_000551.4`, what amino-acid change does each alternative allele cause, and at which position in the protein?
:::

:::{solution} db-c2b-a1-q5
:class: dropdown
Both changes fall on codon **98**, which encodes tyrosine (Y): T>C gives **Y98H** (tyrosine to histidine, TAC→CAC) and T>A gives **Y98N** (tyrosine to asparagine, TAC→AAC). Both are missense; neither truncates the protein.

```{figure} figures/cu2b-dbsnp-details.png
:name: db-fig-cu2b-dbsnp-details
:alt: dbSNP rs5030809, Variant Details.

dbSNP rs5030809, Variant Details. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 6
:label: db-c2b-a1-q6
:nonumber:
The **HGVS** tab gives the position of the variant on the non-coding transcript `NR_176335.1` (`n.`) and on `NM_000551.4` (`c.`), and these are different numbers. Why?
:::

:::{solution} db-c2b-a1-q6
:class: dropdown
The transcript position counts from the first base of the mature RNA, which begins with the 5′ untranslated region. The CDS position counts from the A of the start codon. The difference between the two is the length of the 5′ UTR, which is transcribed but not translated. Here the difference is 70: the variant is at transcript position 362 (`NR_176335.1:n.362`; this transcript starts at the same base as `NM_000551.4`) and coding position c.292, because the 5′ UTR of `NM_000551.4` is 70 nucleotides long. HGVS uses `c.` for coding and `n.` for non-coding numbering precisely to keep the two apart.
:::

:::{exercise} Question 7
:label: db-c2b-a1-q7
:nonumber:
Open **Clinical Significance**. What is reported, for which condition, and what evidence supports it?
:::

:::{solution} db-c2b-a1-q7
:class: dropdown
Both alleles are **pathogenic**. T>C (Y98H) has 17 submissions with no conflicts ("criteria provided, multiple submitters", two stars), for von Hippel-Lindau syndrome and also Chuvash polycythaemia and hereditary cancer predisposition; submitters include diagnostic laboratories such as Ambry Genetics and Labcorp Genetics, and OMIM. T>A (Y98N) rests on a single submission (one star). Name a submitter and its review status rather than repeating the label.

⚠️ **Release-volatile.** *Checked 2026-10-23, ClinVar (live) and dbSNP build 157.*

```{figure} figures/cu2b-dbsnp-clinical.png
:name: db-fig-cu2b-dbsnp-clinical
:alt: dbSNP rs5030809, Clinical Significance.

dbSNP rs5030809, Clinical Significance. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 8
:label: db-c2b-a1-q8
:nonumber:
Both alleles here are missense, yet the variant is classed as pathogenic — whereas many other missense variants are classed as benign. What does that tell you about predicting effect from consequence type alone?
:::

:::{solution} db-c2b-a1-q8
:class: dropdown
Consequence type says what happens to the sequence, not what happens to the protein's job. A missense change at a residue that sits in a binding interface can abolish function, while the same class of change elsewhere is absorbed without consequence. Tyr98 in VHL lies in the β-domain that binds HIF-1α, which is why substitutions there matter.

Classification therefore rests on evidence — functional studies, segregation in families, population frequency — not on the consequence label. That is what the ClinVar review status is summarising.
:::

## Assignment 2: A genetic variant in the VHL gene in dbSNP

We will now look at information related to genotype frequencies in different populations. Since the SNP we are looking at is very rare, we will now focus at the SNP with rs number rs779805, which has a higher minor allele frequency (MAF). Go to the dbSNP database and look up this SNP.

:::{exercise} Question 1
:label: db-c2b-a2-q1
:nonumber:
What type of SNP is this variant? What is its genomic location (in the GRCh38 genome build)? Note whether the variant is in the coding region or not.
:::

:::{solution} db-c2b-a2-q1
:class: dropdown
A single-nucleotide variant (SNV), G>A (and a very rare G>C), at chromosome 3, position 10,141,653 (GRCh38). It is **not** in the coding region: dbSNP now places it just *upstream* of the current VHL transcripts, in the promoter region. On the older transcript version `NM_000551.3` it was described as c.-195G>A, in the 5′ untranslated region, and ClinVar still uses that name; either answer shows it is non-coding.

*Checked 2026-10-23, dbSNP build 157.*
:::

Open the Frequency section; the SNP has been measured in multiple population genetics projects. Looking at the 1000Genomes study, the table shows results per (sub)continent.

:::{exercise} Question 2
:label: db-c2b-a2-q2
:nonumber:
Based on the overview, are the allele frequencies similar or different between different populations?
:::

:::{solution} db-c2b-a2-q2
:class: dropdown
Very different. The alternative allele A has frequency 0.16 in the African population but 0.58–0.82 elsewhere (East Asian 0.82, European 0.70, American 0.60, South Asian 0.58; global 0.54). Outside Africa the *reference* allele G is the less common one. (Use the `1000Genomes` row with n=5008; the `1000Genomes_30X` row gives slightly different numbers.)

```{figure} figures/cu2b-dbsnp-779805-freq.png
:name: db-fig-cu2b-dbsnp-779805-freq
:alt: dbSNP rs779805, Frequency tab.

dbSNP rs779805, Frequency tab. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 3
:label: db-c2b-a2-q3
:nonumber:
Using the allele frequencies of the European population in the 1000Genomes study, what are the genotype frequencies according to the Hardy-Weinberg principle? Assume Z = reference allele and z = alternative allele.

ZZ:

Zz:

zz:
:::

:::{solution} db-c2b-a2-q3
:class: dropdown
European: p = f(G) = 0.297, q = f(A) = 0.703.

- ZZ (GG) = p² = 0.088
- Zz (GA) = 2pq = 0.418
- zz (AA) = q² = 0.494

(With the `1000Genomes_30X` row, p = 0.309: 0.095, 0.427 and 0.478.)

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 4
:label: db-c2b-a2-q4
:nonumber:
Explain how deviations from HW equilibrium might arise for a variant associated with a disease.
:::

:::{solution} db-c2b-a2-q4
:class: dropdown
Hardy–Weinberg equilibrium assumes random mating, no selection, no migration, no new mutation and a large population. A disease-associated variant can deviate because affected genotypes survive or reproduce less (selection), because the sample over-represents patients (ascertainment), because the sample mixes populations with different allele frequencies (stratification), or because of non-random mating such as consanguinity. Genotyping errors also show up as deviations.
:::

:::{exercise} Question 5
:label: db-c2b-a2-q5
:nonumber:
What does ClinVar (via the Clinical Significance tab) say about this variant and von Hippel-Lindau syndrome? Is that plausible, given the allele frequencies you found?
:::

:::{solution} db-c2b-a2-q5
:class: dropdown
ClinVar classifies the variant as **benign** for von Hippel-Lindau syndrome (five submitters, no conflicts). That fits the frequencies: the A allele is carried by the majority of people in most populations, which is impossible for the cause of a rare dominant tumour syndrome. Earlier versions of this assignment asked for a "risk allele"; current evidence gives none.

*Checked 2026-10-23, ClinVar (live) and dbSNP build 157.*
:::

## Assignment 3: The VHL protein in UniProt

Now we turn to the UniProt website, to find more information about the function and structure of the protein encoded by the VHL gene.

First search the human VHL protein in the UniProt database.

:::{exercise} Question 1
:label: db-c2b-a3-q1
:nonumber:
What is the UniProt identifier of the human VHL protein? What is the review status and why is this important?
:::

:::{solution} db-c2b-a3-q1
:class: dropdown
P40337 (entry name VHL_HUMAN, *von Hippel-Lindau disease tumor suppressor*). The entry is **reviewed** (Swiss-Prot): a curator has checked it against the literature, so its annotations are more reliable than those of unreviewed (TrEMBL) entries, which are generated automatically. The function description is supported by four publications with experimental evidence.

*Checked 2026-10-23, UniProt release 2026_03.*
:::

The page starts off with a concise description of the function of the protein, supported by references (verify this). Then information on the GO annotations of the protein is given.

:::{exercise} Question 2
:label: db-c2b-a3-q2
:nonumber:
What is the evidence type associated with the annotation to “negative regulation of cell population proliferation”? Explain what the evidence type means. Is this strong evidence?
:::

:::{solution} db-c2b-a3-q2
:class: dropdown
IDA, *Inferred from Direct Assay* (here contributed via DisProt): a laboratory experiment showed directly that VHL negatively regulates cell proliferation. That is strong evidence, stronger than annotations inferred from sequence similarity (ISS) or assigned electronically (IEA).

```{figure} figures/cu2b-uni-go.png
:name: db-fig-cu2b-uni-go
:alt: UniProt P40337, GO annotations.

UniProt P40337, GO annotations. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 3
:label: db-c2b-a3-q3
:nonumber:
Which general subcellular locations are given by UniProt annotation and which by GO annotation? Identify which subcellular locations are unique to GO annotation.
:::

:::{solution} db-c2b-a3-q3
:class: dropdown
UniProt annotation: cytoplasm, cell membrane, endoplasmic reticulum and nucleus (for isoform 1; isoform 3 is not membrane-associated). GO annotation: cytoplasm, cytosol, endoplasmic reticulum, mitochondrion, nucleoplasm, nucleus, plasma membrane, and the Cul2-RING ubiquitin ligase complex.

Unique to GO: cytosol and nucleoplasm (sub-compartments of cytoplasm and nucleus), **mitochondrion** (the genuinely new location, based only on an author statement, NAS, so weak evidence) and the ubiquitin ligase complex (a protein complex, not a compartment).

```{figure} figures/cu2b-uni-location.png
:name: db-fig-cu2b-uni-location
:alt: UniProt P40337, Subcellular Location.

UniProt P40337, Subcellular Location. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

In the section “Disease & Variants”, we find an overview of involvement of mutations in the protein in human disease.

:::{exercise} Question 4
:label: db-c2b-a3-q4
:nonumber:
What amino acid change (full names) and which location is described for the variant VAR_005676 in the table of disease-causing mutations of von Hippel-Lindau disease? What is the dbSNP ID?
:::

:::{solution} db-c2b-a3-q4
:class: dropdown
Position **70**: **glutamic acid → lysine** (E70K), linked to von Hippel-Lindau disease type I. dbSNP ID: **rs5030802**. (Not the same as rs5030809 from assignment 1, which is UniProt variant VAR_005707, Y98H.)

```{figure} figures/cu2b-uni-variants.png
:name: db-fig-cu2b-uni-variants
:alt: UniProt P40337, variant VAR_005676.

UniProt P40337, variant VAR_005676. Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

Further down on the page, a section is presented on interaction partners of the protein.

:::{exercise} Question 5
:label: db-c2b-a3-q5
:nonumber:
Which protein-protein interaction is supported by the highest number of experiments? What is the biological meaning of this interaction? Is it a subunit of the VCB complex shown below the interaction table?
:::

:::{solution} db-c2b-a3-q5
:class: dropdown
**HIF1A** (23 experiments), followed by CUL2 (19) and ELOB (18). HIF1A is **not** a VCB subunit but the complex's *target*: when oxygen is present, HIF-1α is hydroxylated, VHL binds it, and the VCB–CUL2 E3 ubiquitin ligase (VHL, elongin B, elongin C, CUL2, RBX1) tags it for degradation in the proteasome. Without functional VHL, HIF-1α is not degraded and switches on hypoxia genes, such as those for blood-vessel growth, which is why VHL loss gives highly vascular tumours. CUL2 and ELOB, the next two hits, *are* VCB subunits.

```{figure} figures/cu2b-uni-interaction.png
:name: db-fig-cu2b-uni-interaction
:alt: UniProt P40337, binary interactions (HIF1A ringed).

UniProt P40337, binary interactions (HIF1A ringed). Screenshot of UniProt, 2026-10-28 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

:::{exercise} Question 6
:label: db-c2b-a3-q6
:nonumber:
With the dbSNP ID found in question 4, go to dbSNP and look at its population frequency in the ALFA allele frequency table. In which populations is the alternative allele found, and at what frequency? What does that tell you?
:::

:::{solution} db-c2b-a3-q6
:class: dropdown
In ALFA the alternative allele has been seen once in 13,676 alleles (Total 0.00007; African and African American 0.00008); every other population with data shows 0.000. ExAC has one more observation (Asian, 0.00006, about 1 in 17,000 alleles). This is a rare germline disease mutation, not a common polymorphism, which is what you expect for the cause of a dominant tumour syndrome.

```{figure} figures/cu2b-dbsnp-5030802-freq.png
:name: db-fig-cu2b-dbsnp-5030802-freq
:alt: dbSNP rs5030802, ALFA frequencies.

dbSNP rs5030802, ALFA frequencies. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, dbSNP build 157.*
:::

:::{exercise} Question 7
:label: db-c2b-a3-q7
:nonumber:
Three different nucleotide changes are reported at this position. Which one causes truncation of the protein? What are the effects of the other two? Is the effect the same on all VHL transcripts?
:::

:::{solution} db-c2b-a3-q7
:class: dropdown
- G>T: GAG→**TAG**, a stop codon (p.Glu70Ter, E70\*), so the protein is **truncated**. ClinVar: pathogenic, reviewed by an expert panel.
- G>A: GAG→AAG, glutamic acid → lysine (E70K), missense.
- G>C: GAG→CAG, glutamic acid → glutamine (E70Q), missense.

The effect is the same on all three RefSeq transcripts (`NM_000551.4`, `NM_198156.3`, `NM_001354723.2`), because codon 70 lies in exon 1, which all of them share.

*Checked 2026-10-23, ClinVar (live) and dbSNP build 157.*
:::
