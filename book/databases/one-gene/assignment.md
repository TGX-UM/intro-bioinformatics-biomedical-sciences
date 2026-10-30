(db-p3-a1)=
# Assignment 1: One gene through all six databases

*Time: 80 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

You follow one gene through every database of practicals 1 and 2: NCBI Gene, Ensembl, OMIM, UniProt, WikiPathways and dbSNP/ClinVar. Each version has its own theme. Use the starting points in the table, and write down which source you used for each answer and whether the sources agree. Answer the questions as if you were preparing a short summary of the gene for fellow students. The answers to most questions can be found in more than one database.

| | **Version A** | **Version B** | **Version C** |
|---|---|---|---|
| **Gene** | TP53 | LMNA | APOE |
| **Theme** | Hallmarks of cancer | Hallmarks of ageing | Alzheimer disease |
| **NCBI Gene** | <https://www.ncbi.nlm.nih.gov/gene/7157> | <https://www.ncbi.nlm.nih.gov/gene/4000> | <https://www.ncbi.nlm.nih.gov/gene/348> |
| **Ensembl** | [ENSG00000141510](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000141510) | [ENSG00000160789](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000160789) | [ENSG00000130203](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000130203) |
| **Variant** | rs121912665 | rs58596362 | rs429358 |
| **Pathway** | [WP707](https://www.wikipathways.org/pathways/WP707.html) DNA damage response | [WP4299](https://www.wikipathways.org/pathways/WP4299.html) Lamin A processing | [WP5124](https://www.wikipathways.org/pathways/WP5124.html) Alzheimer's disease |
| **Partner protein** (question 9) | MDM2 | ZMPSTE24 | LRP1 |

## Section 1: Identifiers and basic gene information

:::{exercise} Question 1
:label: db-p3a1-q1
:nonumber:
What are the database identifiers and names for your gene, or the protein it encodes? Are there synonyms for the gene name? Fill in the table, including the URL of each page; you will need all of them in the next questions.

| **Database** | **Identifier** | **Name (gene/protein)** | **Synonyms** | **URL** |
|---|---|---|---|---|
| NCBI Gene | | | | |
| Ensembl | | | | |
| OMIM | | | | |
| UniProt | | | | |
:::

:::{solution} db-p3a1-q1
:class: dropdown
**Version A — TP53**

| Database | Identifier | Name | Synonyms |
|---|---|---|---|
| NCBI Gene | 7157 | tumor protein p53 | BCC7, BMFS5, LFS1, P53, TRP53 |
| Ensembl | ENSG00000141510 | tumor protein p53 | LFS1, P53 |
| OMIM | 191170 | TUMOR PROTEIN p53; TP53 | P53; TRANSFORMATION-RELATED PROTEIN 53; TRP53 |
| UniProt | P04637 | Cellular tumor antigen p53 | Antigen NY-CO-13, Phosphoprotein p53, Tumor suppressor p53 |

**Version B — LMNA**

| Database | Identifier | Name | Synonyms |
|---|---|---|---|
| NCBI Gene | 4000 | lamin A/C | many, including HGPS, CMD1A, FPLD2, LGMD1B, LMN1, PRO1 |
| Ensembl | ENSG00000160789 | lamin A/C | CMD1A, HGPS, LGMD1B, LMN1, LMNL1, MADA, PRO1 |
| OMIM | 150330 | LAMIN A/C; LMNA | |
| UniProt | P02545 | Prelamin-A/C | the mature chains are named Lamin-A/C |

**Version C — APOE**

| Database | Identifier | Name | Synonyms |
|---|---|---|---|
| NCBI Gene | 348 | apolipoprotein E | AD2, APO-E, ApoE4, LDLCQ5, LPG |
| Ensembl | ENSG00000130203 | apolipoprotein E | AD2 |
| OMIM | 107741 | APOLIPOPROTEIN E; APOE | |
| UniProt | P02649 | Apolipoprotein E (Apo-E) | |

Notice how the synonym lists differ between databases: some synonyms are disease names (LFS1 = Li-Fraumeni syndrome 1, HGPS = Hutchinson-Gilford progeria syndrome, AD2 = Alzheimer disease 2). The identifiers are what stay stable.

*Checked 2026-10-23 (NCBI Gene, Ensembl, UniProt release 2026_03); OMIM names checked by hand 2026-10-24.*
:::

:::{exercise} Question 2
:label: db-p3a1-q2
:nonumber:
On which chromosome, and on which strand, is your gene located?
:::

:::{solution} db-p3a1-q2
:class: dropdown
- **A — TP53:** chromosome 17 (17p13.1), reverse (minus) strand.
- **B — LMNA:** chromosome 1 (1q22), forward (plus) strand.
- **C — APOE:** chromosome 19 (19q13.32), forward (plus) strand.

*Checked 2026-10-23, Ensembl and NCBI Gene.*
:::

## Section 2: A disease-associated variant

:::{exercise} Question 3
:label: db-p3a1-q3
:nonumber:
Look up the variant given in the table for your version.

a) Find the variant in OMIM: open your gene's entry, go to **Allelic Variants** and use the **Table View**. Which disease is it linked to, and what amino-acid change does OMIM give?

b) Open the variant in dbSNP. Which alleles are reported at this position? Does the change OMIM describes match one of them?

c) What is the molecular consequence of each allele on the MANE Select transcript? Compare dbSNP with Ensembl's variant page (search the rsID at <https://www.ensembl.org/search>, then step through the alleles).

d) How is the variant classified clinically in ClinVar (follow the link from dbSNP)? Do the classifications agree with OMIM?

e) What is the global allele frequency, and which datasets report it? Is that frequency what you would expect, given the disease?
:::

:::{solution} db-p3a1-q3
:class: dropdown
**Version A — TP53, rs121912665**

- a) Allelic variant 191170.0038: colorectal cancer, TP53 Ala189Val.
- b) dbSNP reports G>A, G>C and G>T at chr17:7,674,965. TP53 lies on the reverse strand, so on the transcript these are c.566C>T, C>G and C>A. OMIM's change is the G>A allele.
- c) All three alleles are **missense**: p.Ala189Val, p.Ala189Gly and p.Ala189Asp. Ensembl gives the same consequence per allele.
- d) This is the interesting part. The OMIM-derived ClinVar record still says "pathogenic" for familial colorectal cancer, but without assertion criteria. Laboratories have since submitted other interpretations, so ClinVar's overall classification is now **conflicting**, and the two other alleles are of **uncertain significance**. An old literature report and the current clinical evidence disagree, and ClinVar shows both.
- e) Extremely rare: no 1000 Genomes frequency at all, and about 7 (gnomAD genomes) to 29 (gnomAD exomes) in a million alleles. That is expected for a variant in a tumour suppressor that is under suspicion of causing cancer.

**Version B — LMNA, rs58596362**

- a) Allelic variant 150330.0022: Hutchinson-Gilford progeria syndrome (HGPS), with restrictive dermopathy 2 included: Gly608Gly, a change that does *not* alter the amino acid. It is the classic HGPS variant, but not the only one: OMIM lists more LMNA variants that cause HGPS.
- b) dbSNP reports C>T and C>A at chr1:156,138,613. OMIM's change is the C>T allele (c.1824C>T).
- c) Both alleles are **synonymous** (p.Gly608=): the protein sequence is unchanged.
- d) C>T is **pathogenic** (multiple submitters, no conflicts) for Hutchinson-Gilford progeria; C>A is **likely benign**. The point of this version: a synonymous change can still cause disease. C>T activates a hidden splice site in exon 11, and the resulting mRNA lacks 150 nucleotides. The protein made from it, progerin, misses 50 amino acids, including the site where ZMPSTE24 cuts (see question 10). The consequence label "synonymous" only describes the codon, not what happens to splicing.
- e) Not seen in 1000 Genomes. The gnomAD and TOPMed frequencies shown (a few per million) belong to the C>A allele; the pathogenic C>T allele has no frequency in any dataset. HGPS is extremely rare, and nearly always arises as a new (de novo) mutation in the child.

**Version C — APOE, rs429358**

- a) Allelic variant 107741.0016: "Alzheimer disease 2 due to APOE4 isoform", APOE Cys112Arg. OMIM uses the classic numbering of the *mature* protein. It lists two SNPs, rs429358 and rs7412, because the three common APOE alleles are defined by two positions together: ε4 carries Arg at 112 (rs429358) and Arg at 158 (rs7412), ε3 has Cys112/Arg158 and ε2 Cys112/Cys158.
- b) dbSNP reports T>C at chr19:44,908,684. In dbSNP and ClinVar the change is called p.Cys130Arg. The difference of 18 is the signal peptide, which is counted in the precursor (dbSNP) but cut off in the mature protein (OMIM). Same variant, two numbering systems.
- c) **Missense** (p.Cys130Arg); Ensembl agrees.
- d) ClinVar does not call it plainly "pathogenic": it lists it as a **risk factor**, with conflicting and "other" entries. That fits a common risk allele: carrying ε4 increases the chance of late-onset Alzheimer disease, but does not cause it on its own.
- e) **Common**: 0.15 globally in 1000 Genomes (African 0.27, European 0.16, East Asian 0.09, South Asian 0.09, American 0.10). That is very different from versions A and B, and expected, because a risk allele for a disease of old age is not strongly removed by selection.

⚠️ **Release-volatile** — ClinVar classifications change. *Checked 2026-10-23 (frequencies 2026-10-28), dbSNP build 157, ClinVar (live), Ensembl (Release 2026-07). OMIM allelic variants checked by hand 2026-10-24.*

```{figure} ../figures/2b-train-A-dbsnp.png
:name: db-fig-2b-train-A-dbsnp
:alt: Version A: dbSNP rs121912665.

Version A: dbSNP rs121912665. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2b-train-B-dbsnp.png
:name: db-fig-2b-train-B-dbsnp
:alt: Version B: dbSNP rs58596362.

Version B: dbSNP rs58596362. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2b-train-C-dbsnp.png
:name: db-fig-2b-train-C-dbsnp
:alt: Version C: dbSNP rs429358.

Version C: dbSNP rs429358. Screenshot of dbSNP, 2026-10-23 (NCBI, public domain).
```
:::

## Section 3: Transcripts and isoforms

:::{exercise} Question 4
:label: db-p3a1-q4
:nonumber:
Look up the transcripts / isoforms (splice variants) of your gene in Ensembl (use the **Transcripts table** view), UniProt and NCBI (RefSeq section), and fill in the table.

| **Database** | **Total number of transcripts / isoforms** | **Number of protein-coding transcripts** |
|---|---|---|
| Ensembl | | |
| UniProt | | |
| NCBI RefSeq | | |
:::

:::{solution} db-p3a1-q4
:class: dropdown
| | Ensembl: total / protein coding | UniProt isoforms | NCBI RefSeq: curated transcripts / proteins |
|---|---|---|---|
| **A — TP53** | 40 / 34 | 9 | 26 (25 NM\_ + 1 NR\_) / 25 NP\_ |
| **B — LMNA** | 84 / 39 | 6 (one of them, isoform 6, is progerin) | 28 NM\_ / 28 NP\_ |
| **C — APOE** | 39 / 38 | 1 | 5 NM\_ / 5 NP\_ |

The three numbers do not agree, and that is the answer to the next question rather than a mistake. Ensembl counts **annotated transcript models**, including non-coding ones and models supported by newer long-read data. NCBI RefSeq counts **curated reference transcripts**, a deliberately more conservative set. UniProt counts **distinct protein isoforms**: transcripts that encode the same protein collapse into one.

For APOE, note that the well-known E2, E3 and E4 forms are *not* isoforms. They are the same protein from different alleles (polymorphisms), which is why UniProt lists one isoform.

⚠️ **Release-volatile** — all three change between releases, and Ensembl's counts changed even between August and October 2026 while its release label stayed the same. Quote a number with the database, the release or gene version (e.g. ENSG00000141510.21) and the date. *Checked 2026-10-23 (Ensembl, UniProt release 2026_03, NCBI RefSeq annotation RS_2025_08).*

```{figure} ../figures/2b-train-A-ens-tx.png
:name: db-fig-2b-train-A-ens-tx
:alt: Version A: Ensembl, TP53 Transcripts table (first rows).

Version A: Ensembl, TP53 Transcripts table (first rows). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

```{figure} ../figures/2b-train-B-ens-tx.png
:name: db-fig-2b-train-B-ens-tx
:alt: Version B: Ensembl, LMNA Transcripts table (first rows).

Version B: Ensembl, LMNA Transcripts table (first rows). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

```{figure} ../figures/2b-train-C-ens-tx.png
:name: db-fig-2b-train-C-ens-tx
:alt: Version C: Ensembl, APOE Transcripts table (first rows).

Version C: Ensembl, APOE Transcripts table (first rows). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```
:::

:::{exercise} Question 5
:label: db-p3a1-q5
:nonumber:
Which transcript is labelled **MANE Select** in Ensembl, and which in NCBI? Is it the same transcript? Why is it useful that the two databases agree on one transcript?
:::

:::{solution} db-p3a1-q5
:class: dropdown
- **A — TP53:** ENST00000269305 = NM_000546.6 (protein NP_000537.3, 393 aa).
- **B — LMNA:** ENST00000368300 = NM_170707.4 (lamin A, 664 aa). LMNA also has a second MANE transcript, **MANE Plus Clinical** NM_005572.4 (lamin C, 572 aa), because clinically important variants are reported on it too.
- **C — APOE:** ENST00000252486 = NM_000041.4 (protein NP_000032.1, 317 aa).

Yes, it is the same transcript: MANE (Matched Annotation from NCBI and EMBL-EBI) is a joint project in which both institutes agree on one representative transcript per gene, identical in sequence in both databases. Variants, such as those in question 3, are reported on this transcript, so everyone describes the same change in the same way.

*Checked 2026-10-23, Ensembl and NCBI RefSeq.*
:::

:::{exercise} Question 6
:label: db-p3a1-q6
:nonumber:
How can you verify that two isoforms with different labels (e.g. "isoform a" vs "isoform 1") represent the same protein?
:::

:::{solution} db-p3a1-q6
:class: dropdown
Compare their sequences: the only reliable way is to align the amino-acid (or nucleotide) sequences. Labels and numbering differ between databases, so matching names is not enough. Cross-references help: RefSeq NP\_ IDs, UniProt isoform IDs (such as P04637-1) and MANE Select are the most consistent anchors between databases.
:::

## Section 4: Expression and protein

:::{exercise} Question 7
:label: db-p3a1-q7
:nonumber:
Using NCBI Gene, which tissues show the highest expression of your gene? Name the top three. (In the **Expression** section, select the HPA RNA-seq normal-tissue dataset in the drop-down; it may open on a different dataset.)
:::

:::{solution} db-p3a1-q7
:class: dropdown
- **A — TP53:** spleen, lymph node, skin. The differences are small: TP53 is expressed broadly.
- **B — LMNA:** gall bladder, skin, lung. Also broad.
- **C — APOE:** liver, kidney, adrenal gland. Liver stands out (about 1,000 TPM).

⚠️ **Release-volatile.** *Checked 2026-10-23, NCBI Gene, HPA RNA-seq normal tissues.*
:::

:::{exercise} Question 8
:label: db-p3a1-q8
:nonumber:
Summarise the functional descriptions of your gene from NCBI Gene (Summary) and UniProt (Function). Note one similarity and one difference in their emphasis. What does UniProt say about where the protein is expressed (section **Expression**, "Tissue specificity")?
:::

:::{solution} db-p3a1-q8
:class: dropdown
In general, NCBI gives a broad summary of what the gene does and which diseases it is linked to, while UniProt gives a more detailed, mechanistic and protein-centred description, with interaction partners, isoforms and evidence.

- **A — TP53:** both describe a transcription factor that acts as a tumour suppressor, inducing cell-cycle arrest, DNA repair or apoptosis in response to stress. UniProt adds isoform-specific functions and many interaction partners. Tissue specificity: "Ubiquitous", with isoforms expressed in a tissue-dependent manner.
- **B — LMNA:** both describe lamins as the proteins that form the nuclear lamina, the meshwork under the inner nuclear membrane; only UniProt calls them intermediate-filament proteins. NCBI stresses the many diseases (laminopathies). Tissue specificity: UniProt only mentions that prelamin A accumulates with age and in atherosclerotic vascular smooth-muscle cells, a direct link to ageing.
- **C — APOE:** both describe an apolipoprotein that transports lipids, especially cholesterol, between organs. NCBI stresses the clearance of chylomicron and VLDL remnants and type III hyperlipoproteinemia; neither text mentions Alzheimer disease. Tissue specificity: mainly made by liver hepatocytes, but also in large amounts in the brain, mainly by astrocytes.

*Checked 2026-10-28, NCBI Gene and UniProt release 2026_03.*
:::

:::{exercise} Question 9
:label: db-p3a1-q9
:nonumber:
Does UniProt report a direct interaction between your protein and the **partner protein** in the table? (UniProt, section **Interaction**, Binary interactions.) Look for the partner in your pathway in question 10: what does the pathway say about the two of them?
:::

:::{solution} db-p3a1-q9
:class: dropdown
Yes, in all three versions the partner is listed among the binary interactions:

- **A:** TP53–MDM2. MDM2 is the main negative regulator of p53.
- **B:** LMNA–ZMPSTE24. ZMPSTE24 is the protease that processes prelamin A.
- **C:** APOE–LRP1. LRP1 is a receptor through which APOE-containing lipoproteins and amyloid-β are taken up by cells.

How many interaction partners UniProt lists differs a lot: TP53 has 187, LMNA 94, APOE 47.

```{figure} ../figures/2b-train-A-uni-interaction.png
:name: db-fig-2b-train-A-uni-interaction
:alt: Version A: UniProt P04637, binary interactions (MDM2 ringed).

Version A: UniProt P04637, binary interactions (MDM2 ringed). Screenshot of UniProt, 2026-10-23 (CC BY 4.0).
```

```{figure} ../figures/2b-train-B-uni-interaction.png
:name: db-fig-2b-train-B-uni-interaction
:alt: Version B: UniProt P02545, binary interactions (ZMPSTE24 ringed).

Version B: UniProt P02545, binary interactions (ZMPSTE24 ringed). Screenshot of UniProt, 2026-10-28 (CC BY 4.0).
```

```{figure} ../figures/2b-train-C-uni-interaction.png
:name: db-fig-2b-train-C-uni-interaction
:alt: Version C: UniProt P02649, binary interactions (LRP1 ringed).

Version C: UniProt P02649, binary interactions (LRP1 ringed). Screenshot of UniProt, 2026-10-28 (CC BY 4.0).
```

*Checked 2026-10-23, UniProt release 2026_03.*
:::

## Section 5: Pathways and functional context

:::{exercise} Question 10
:label: db-p3a1-q10
:nonumber:
Open the pathway for your version (see the table). Find your gene and the partner protein in the diagram. What happens between them, and what kind of interaction (arrow type) is shown? Which other protein acts on your gene product?
:::

:::{solution} db-p3a1-q10
:class: dropdown
- **A — TP53, WP707 DNA damage response:** MDM2 → TP53 is drawn with a **T-bar**, meaning inhibition: MDM2 marks p53 for degradation. **ATM** → TP53 is an arrow, meaning activation: DNA damage, sensed by ATM, switches p53 on. TP53 in turn activates CDKN1A (p21), GADD45 and pro-apoptotic genes (BAX, BBC3, PMAIP1).
- **B — LMNA, WP4299 Lamin A processing:** LMNA is translated into **pre-lamin A**, which is processed in steps. Farnesyl transferase attaches a farnesyl group to the C-terminal CaaX motif, the last three amino acids are removed (in this diagram also by ZMPSTE24) and the end is methylated, and finally ZMPSTE24 (drawn as "CAAX prenyl protease 1 homolog") cuts off the last 15 amino acids, farnesyl group included. That gives mature lamin A. There is no direct LMNA–ZMPSTE24 arrow: each enzyme is joined to the step it catalyses by a line ending in a small open circle (catalysis). The pathway marks the link to progeria: progerin lacks the second ZMPSTE24 cleavage site and stays permanently farnesylated (question 3).
- **C — APOE, WP5124 Alzheimer's disease:** amyloid-β (Aβ40 and Aβ42) → APOE, then APOE → LRP1, arrows meaning a positive link. APOE binds amyloid-β and carries it to the receptor LRP1 for clearance from the brain. The ε4 form of APOE does this less efficiently.

```{figure} ../figures/2b-train-A-wp707.png
:name: db-fig-2b-train-A-wp707
:alt: Version A: WP707, TP53 and MDM2 ringed.

Version A: WP707, TP53 and MDM2 ringed. Figure from WikiPathways WP707 (CC0).
```

```{figure} ../figures/2b-train-B-wp4299.png
:name: db-fig-2b-train-B-wp4299
:alt: Version B: WP4299, LMNA and ZMPSTE24 ringed.

Version B: WP4299, LMNA and ZMPSTE24 ringed. Figure from WikiPathways WP4299 (CC0).
```

```{figure} ../figures/2b-train-C-wp5124.png
:name: db-fig-2b-train-C-wp5124
:alt: Version C: WP5124, APOE and LRP1 ringed.

Version C: WP5124, APOE and LRP1 ringed. Figure from WikiPathways WP5124 (CC0).
```

*Checked 2026-10-28, WikiPathways.*
:::

:::{exercise} Question 11
:label: db-p3a1-q11
:nonumber:
Using UniProt's GO annotations (section **Function**, GO annotations → Biological Process), give one biological process supported by **IDA** evidence (Inferred from Direct Assay). Provide the GO ID. What does IDA evidence mean, compared with evidence that was predicted?
:::

:::{solution} db-p3a1-q11
:class: dropdown
Many answers are possible; examples:

- **A — TP53:** DNA damage response, GO:0006974.
- **B — LMNA:** nuclear envelope organization, GO:0006998.
- **C — APOE:** cholesterol efflux, GO:0033344.

IDA means a laboratory experiment showed the process directly for this protein. That is stronger than annotations inferred from sequence similarity or by computation (for example IEA, electronic annotation).

*Checked 2026-10-23, UniProt release 2026_03.*
:::

## Section 6: Phenotypes and inheritance

12) Which phenotypes or diseases are associated with your gene in OMIM (Gene–Phenotype table), NCBI Gene (Phenotypes), ClinVar and UniProt (Disease & Variants)? What do these phenotypes have in common?

:::{exercise} Question 13
:label: db-p3a1-q13
:nonumber:
What inheritance pattern does OMIM give for the main disease of your version (A: Li-Fraumeni syndrome; B: Hutchinson-Gilford progeria; C: Alzheimer disease 2)? Does UniProt say the same?
:::

:::{solution} db-p3a1-q13
:class: dropdown
**Version A — TP53:** mostly cancers and cancer predisposition: Li-Fraumeni syndrome, colorectal cancer, breast cancer, hepatocellular carcinoma, osteosarcoma, adrenocortical carcinoma, choroid plexus papilloma and others, plus bone marrow failure syndrome 5. Li-Fraumeni syndrome is **autosomal dominant** in OMIM, and UniProt says the same. Many of the other entries concern somatic mutations, acquired in the tumour rather than inherited.

**Version B — LMNA:** a striking variety, the "laminopathies": Hutchinson-Gilford progeria, dilated cardiomyopathy, Emery-Dreifuss muscular dystrophy (dominant and recessive forms), familial partial lipodystrophy, Charcot-Marie-Tooth disease type 2B1, mandibuloacral dysplasia and others. What they share is the nuclear lamina, but different tissues are hit by different variants. For HGPS, OMIM gives **autosomal dominant**, nearly always a new (de novo) mutation; UniProt states no inheritance for HGPS.

**Version C — APOE:** lipid disorders (hyperlipoproteinemia type III, lipoprotein glomerulopathy, sea-blue histiocyte disease), Alzheimer disease ("Alzheimer disease 2, due to APOE4", and a provisional modifier entry for the APOE3-Christchurch variant), coronary artery disease susceptibility and age-related macular degeneration. OMIM gives Alzheimer disease 2 as **autosomal dominant**, but that needs care: ε4 is a risk allele, not a Mendelian cause. Many carriers never develop the disease and many patients do not carry it. UniProt only describes ε4 as genetically *associated* with late-onset Alzheimer disease. Compare the braces OMIM puts around "{Coronary artery disease, severe, susceptibility to}": that is how OMIM normally marks a risk phenotype.

*Checked 2026-10-23 for NCBI Gene, ClinVar and UniProt release 2026_03; OMIM tables checked by hand 2026-10-24.*
:::

## Section 7: Integration

:::{exercise} Question 14
:label: db-p3a1-q14
:nonumber:
Compare the tissues where your gene is most highly expressed (question 7) with the phenotypes associated with it (questions 12–13). Is expression level a good predictor of disease involvement? Explain.
:::

:::{solution} db-p3a1-q14
:class: dropdown
No, not in any of the three versions.

- **A — TP53:** broadly expressed, and cancers arise in many tissues; disease comes from loss of function, not from where the gene is most expressed.
- **B — LMNA:** highest in gall bladder, skin and lung, but the diseases hit heart, skeletal muscle, fat tissue, nerves and, in progeria, the whole body.
- **C — APOE:** highest in liver, while the best-known disease is in the brain. The brain's APOE is made by astrocytes and does not show up as a peak in a whole-tissue table.

Disease involvement depends on what a variant does to the protein, on which tissues depend on that protein, and on age, not on the expression level alone.
:::

:::{exercise} Question 15
:label: db-p3a1-q15
:nonumber:
**Compare with another version.** Put your answers to questions 3e, 4 and 13 next to those of a classmate who chose a different version (or next to your own answers for a second version). How do the genes differ in number of transcripts, in how common the variant is, and in how the disease is inherited? What does the comparison of TP53 or LMNA with APOE tell you about the difference between a disease-causing variant and a risk allele?
:::

:::{solution} db-p3a1-q15
:class: dropdown
- **Transcripts:** LMNA has by far the most annotated transcripts in Ensembl (84), TP53 and APOE about 40, while UniProt lists 9, 6 and 1 isoforms. Annotation depth and protein diversity are different things.
- **Variant frequency:** the TP53 and LMNA variants are extremely rare, while APOE ε4 is carried by about 1 in 7 alleles worldwide.
- **Inheritance:** Li-Fraumeni syndrome and HGPS follow a dominant pattern (for HGPS nearly always de novo). OMIM also lists Alzheimer disease 2 as dominant, but ε4 only raises risk: many carriers never develop the disease and many patients do not carry it.

A disease-causing variant with a strong effect stays rare, because it is removed by selection. A risk allele with a modest effect, acting late in life, can become common. Both appear in ClinVar, but with very different labels ("pathogenic" versus "risk factor").
:::
