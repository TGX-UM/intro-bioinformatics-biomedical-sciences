(db-catch-up-2a)=
# Extra practice: catch-up assignment 2A

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

BBS2002 students who missed the 2A computer session do this assignment instead. For everyone
else it is extra practice with the databases of practical 2A, on a new example. It does not
replace the original assignments and does not cover all their content.

In these assignments you study sphingolipid-related processes as an example. Sphingolipids are a
class of lipids including sphingosine. They are associated with sphingolipidoses, a class of
diseases related to intellectual disability, neurodegeneration and other symptoms.

*Background: the [Reference guide](guide/index.md) has one page per database.*

## Assignment 1: Sphingolipid metabolism in WikiPathways

Look up the human [*Sphingolipid* pathway](https://www.wikipathways.org/pathways/WP1422.html) in WikiPathways ([wikipathways.org/pathways/WP1422](https://www.wikipathways.org/pathways/WP1422.html)).

:::{exercise} Question 1
:label: db-c2a-a1-q1
:nonumber:
When was the pathway last updated?
:::

:::{solution} db-c2a-a1-q1
:class: dropdown
Read the date off the *last edited* badge on the pathway page. At the time of writing that was 7 March 2025.

⚠️ **Release-volatile** — the date moves with every edit.

```{figure} figures/cu2a-wp1422-page.png
:name: db-fig-cu2a-wp1422-page
:alt: WikiPathways WP1422, pathway page.

WikiPathways WP1422, pathway page. Figure from WikiPathways WP1422 (CC0).
```

*Checked 2026-10-23, WikiPathways WP1422.*
:::

:::{exercise} Question 2
:label: db-c2a-a1-q2
:nonumber:
The CERT protein is involved in multiple conversions within this pathway. Name two distinct conversions involving CERT.
:::

:::{solution} db-c2a-a1-q2
:class: dropdown
CERT appears in three places in the diagram and is linked to four conversions; any two count:

- ceramide → sphingomyelin;
- ceramide → galactosylceramide (GalCer);
- dihydroceramide → dihydrosphingomyelin (DHSM);
- dihydroceramide → dihydroglucosylceramide (DHGlcCer).

```{figure} figures/cu2a-wp1422.png
:name: db-fig-cu2a-wp1422
:alt: WikiPathways WP1422, CERT ringed.

WikiPathways WP1422, CERT ringed. Figure from WikiPathways WP1422 (CC0).
```

*Checked 2026-10-23, WikiPathways WP1422.*
:::

:::{exercise} Question 3
:label: db-c2a-a1-q3
:nonumber:
What biological role does CERT have in these conversions?
:::

:::{solution} db-c2a-a1-q3
:class: dropdown
CERT is not an enzyme but a **transfer protein**: it carries ceramide (and dihydroceramide) from the endoplasmic reticulum, where it is made, to the Golgi apparatus, where enzymes such as sphingomyelin synthase convert it. Without CERT the substrate does not reach the enzyme. Note that the diagram draws CERT with the same arrow type as the enzymes (catalysis), so the diagram alone does not tell you it is a transporter; UniProt does (GO: *ER to Golgi ceramide transport*).

*Checked 2026-10-23, WikiPathways WP1422.*
:::

:::{exercise} Question 4
:label: db-c2a-a1-q4
:nonumber:
Name a protein that has an opposing effect of CERT, based on the pathway. Explain how the two proteins together regulate sphingolipid homeostasis.
:::

:::{solution} db-c2a-a1-q4
:class: dropdown
Several answers are defensible. The clearest in the diagram is **glucosylceramidase (GBA)**, which converts glucosylceramide back into ceramide, the reverse of a step CERT supplies. The diagram also draws a sphingomyelin → ceramide step, but labels it with SGMS1/SGMS2, which are sphingomyelin *synthases*; biologically this reverse step is carried out by **sphingomyelinases**, so that answer is right on biological grounds even though the label is odd (a curation issue in the diagram).

Together, CERT-supplied synthesis and these breakdown steps keep the balance between ceramide (which in excess promotes stress responses and apoptosis) and complex sphingolipids such as sphingomyelin (which are needed for membranes).

*Checked 2026-10-23, WikiPathways WP1422.*
:::

:::{exercise} Question 5
:label: db-c2a-a1-q5
:nonumber:
The pathway is cited by two papers (see *Cited in* on the pathway page). Summarise how this pathway was cited and for which reason. What did the authors of these papers find regarding this pathway? Explain this for both papers.
:::

:::{solution} db-c2a-a1-q5
:class: dropdown
- Momin et al. (2011), *J Lipid Res*, doi:10.1194/jlr.M010454: a method to visualise 'omics' data on sphingolipid-metabolism diagrams, to spot interesting differences between samples. This paper is closely tied to the pathway itself: the diagram is used as the map on which transcript and metabolite data are shown.
- Cooper et al. (2016), *PLoS One*, doi:10.1371/journal.pone.0164438: long-term culture of the A549 lung cancer cell line made the cells form lamellar bodies and become more like alveolar type II cells (the surfactant-producing cells of the lung); the sphingolipid pathway was used to interpret changes in gene expression in lipid metabolism.

Students should describe in their own words what each paper used the pathway for.

*Checked 2026-10-23, WikiPathways and the papers' abstracts.*
:::

:::{exercise} Question 6
:label: db-c2a-a1-q6
:nonumber:
CERT is involved in a key regulatory feedback mechanism controlling ceramide and sphingomyelin levels. Describe the biological consequence of dysregulated CERT activity on cell membranes.
:::

:::{solution} db-c2a-a1-q6
:class: dropdown
If CERT is too active, too much ceramide is moved to the Golgi and converted into sphingomyelin; if it is too little active, ceramide accumulates in the ER and less sphingomyelin is made. Because sphingomyelin and cholesterol together form ordered membrane domains (lipid rafts), changes in either direction alter membrane composition, fluidity and signalling, and accumulating ceramide can trigger stress responses and cell death. CERT itself is switched off by phosphorylation when sphingomyelin levels are sufficient, which is the feedback loop the question refers to (not shown in the diagram).
:::

Click on the CERT box in the pathway diagram, which brings you to a different database.

:::{exercise} Question 7
:label: db-c2a-a1-q7
:nonumber:
What are the Ensembl identifier and HGNC accession number of the human CERT gene?
:::

:::{solution} db-c2a-a1-q7
:class: dropdown
Ensembl: ENSG00000113163. HGNC: HGNC:2205 (symbol CERT1, *ceramide transporter 1*; previous symbol COL4A3BP).

*Checked 2026-10-23, Ensembl and HGNC.*
:::

:::{exercise} Question 8
:label: db-c2a-a1-q8
:nonumber:
What is the chromosomal location and strand of this gene, according to Ensembl? Which version of the human genome assemblies is used?
:::

:::{solution} db-c2a-a1-q8
:class: dropdown
Chromosome 5: 75,356,345–75,512,138, reverse strand, on assembly GRCh38 (GRCh38.p14, GCA_000001405.29). NCBI gives slightly different coordinates (75,368,486–75,511,981) because the two databases include different transcripts in the gene, and Ensembl's longest transcripts start further out.

```{figure} figures/cu2a-ens-cert1.png
:name: db-fig-cu2a-ens-cert1
:alt: Ensembl, CERT1 gene page.

Ensembl, CERT1 gene page. Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl gene ENSG00000113163.20.*
:::

## Assignment 2: genetic variants in the CERT1 gene in OMIM

Open the OMIM page for this gene.

:::{exercise} Question 1
:label: db-c2a-a2-q1
:nonumber:
What is the OMIM identifier for CERT1?
:::

:::{solution} db-c2a-a2-q1
:class: dropdown
604677

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 2
:label: db-c2a-a2-q2
:nonumber:
To which condition has the gene been associated? What is the OMIM ID of this phenotype? What is the inheritance pattern? What is the link between CERT1 and this phenotype?
:::

:::{solution} db-c2a-a2-q2
:class: dropdown
A neurodevelopmental disorder, OMIM **616351**. OMIM has renamed it: it is now *Neurodevelopmental disorder with hypotonia, speech delay, and dysmorphic facies* (NEDHSF), formerly *intellectual developmental disorder, autosomal dominant 34* (the older name is still used in ClinVar). Inheritance: **autosomal dominant**, usually by new (de novo) mutations. The disease variants cluster in a short serine-rich stretch of CERT1 that is normally phosphorylated to switch the protein off; the mutant protein stays active, so too much ceramide is transported, which disturbs sphingolipid balance in the developing brain.

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 3
:label: db-c2a-a2-q3
:nonumber:
Name one paper that is mentioned in the expert-written text in OMIM and has studied the association with the condition.
:::

:::{solution} db-c2a-a2-q3
:class: dropdown
Any paper cited in the OMIM text that studies patients with CERT1 variants is acceptable, for example:

- the Deciphering Developmental Disorders Study (2015): three unrelated boys with the same de novo variant, S132L (.0001);
- Murakami et al. (2020): a 23-year-old woman with a de novo S135P variant (.0002), with cell studies showing that the mutant protein is no longer phosphorylated and so stays permanently active;
- Gehin et al. (2023): 21 unrelated patients with de novo CERT1 missense variants.

*Checked 2026-10-24, OMIM checked by hand.*
:::

Open the Table View of Allelic Variants for the CERT1 gene from the left-side menu.

:::{exercise} Question 4
:label: db-c2a-a2-q4
:nonumber:
What are the OMIM identifiers of the mutations described, and which changes occur?
:::

:::{solution} db-c2a-a2-q4
:class: dropdown
Five allelic variants, all amino-acid substitutions (missense):

- 604677.0001: Ser132Leu;
- 604677.0002: Ser135Pro;
- 604677.0003: Ser138Cys;
- 604677.0004: Thr166Ala;
- 604677.0005: Gly243Arg.

Three of them hit serines in the same short region, the phosphorylation site that normally inactivates CERT.

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 5
:label: db-c2a-a2-q5
:nonumber:
One of the variants has a SNP identifier. What is the dbSNP identifier of this variant? Explain what SNP means.
:::

:::{solution} db-c2a-a2-q5
:class: dropdown
Variant .0001 (Ser132Leu) has dbSNP identifier **rs1064794019**. SNP means *single nucleotide polymorphism*: a position in the genome where people differ by one base. Strictly, "polymorphism" means a variant that is common in the population (frequency above about 1%); dbSNP collects all short variants, rare and common, under rs numbers, so a rare disease variant like this one also has an rs number.

Note that ClinVar now classifies this variant as *conflicting*, not plainly pathogenic.

*Checked 2026-10-24, OMIM checked by hand.*
:::

Now go back to the main page of the CERT1 gene, and click the OMIM identifier of the associated condition (616351) in the table.

:::{exercise} Question 6
:label: db-c2a-a2-q6
:nonumber:
Are other genes associated to the syndrome, as described in OMIM? Which one(s)?
:::

:::{solution} db-c2a-a2-q6
:class: dropdown
No. NCBI links phenotype 616351 only to CERT1; the OMIM page should show CERT1 as the only gene.

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 7
:label: db-c2a-a2-q7
:nonumber:
What are the characteristics of a patient that has this syndrome?
:::

:::{solution} db-c2a-a2-q7
:class: dropdown
As the new name says: developmental delay with intellectual disability (mild to profound), low muscle tone (hypotonia) with delayed or absent walking, poor or absent speech, and characteristic (dysmorphic) facial features. Other common features in OMIM's *Clinical Features*: feeding difficulties and poor growth in infancy, behavioural problems (autism spectrum disorder, ADHD, stereotypic or self-injurious behaviour), seizures in about half of the patients, and on brain imaging a thin corpus callosum and delayed myelination.

*Checked 2026-10-24, OMIM checked by hand.*
:::

## Assignment 3: Genetic and functional information on CERT1 in Ensembl

Now open the Ensembl page for the human CERT1 gene: <https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000113163>. Ensembl rebuilt its website in 2026; gene pages are now shown in the app called the Feature explorer. The counts below change as the annotation is updated, so note the gene version shown on the page (the number after the dot in the gene ID).

:::{exercise} Question 1
:label: db-c2a-a3-q1
:nonumber:
Switch to the **Genome browser** (the "View in" button on the gene page). Which other genes are in the same genomic region as the CERT1 gene? Name 5 genes. Are they on the same DNA strand?
:::

:::{solution} db-c2a-a3-q1
:class: dropdown
Any five neighbouring genes read off the browser are acceptable; the list depends on how far you zoom out, so say how wide a window you used. The strand is shown by the arrowheads on each gene and by the track it is drawn in (forward-strand genes above the sequence line, reverse-strand genes below). CERT1 is on the reverse strand. Neighbouring genes do not have to share a strand: each gene is read from its own strand.
:::

:::{exercise} Question 2
:label: db-c2a-a3-q2
:nonumber:
Switch to the **Transcripts table** view. How many transcripts (splice variants) are known for this gene? How many are protein coding?
:::

:::{solution} db-c2a-a3-q2
:class: dropdown
37 transcripts, of which 29 are protein coding. The others are 5 nonsense-mediated-decay transcripts, 2 retained introns and 1 `protein_coding_CDS_not_defined`.

⚠️ **Release-volatile.** *Checked 2026-10-23, Ensembl gene ENSG00000113163.20.*

```{figure} figures/cu2a-ens-cert1-tx.png
:name: db-fig-cu2a-ens-cert1-tx
:alt: Ensembl, CERT1 Transcripts table (first rows).

Ensembl, CERT1 Transcripts table (first rows). Screenshot of Ensembl, 2026-10-23 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```
:::

:::{exercise} Question 3
:label: db-c2a-a3-q3
:nonumber:
Which transcript is the longest in base pairs (cDNA length)? Which transcript codes for the protein with the most amino acids? Give their Ensembl IDs. Explain why these are not the same transcript.
:::

:::{solution} db-c2a-a3-q3
:class: dropdown
Longest in base pairs: ENST00000644072.2, 8,012 bp, which encodes a protein of 624 amino acids. Longest protein: ENST00000405807.10, 752 amino acids. (The MANE Select transcript is ENST00000643780.2: 3,868 bp, also 624 amino acids.)

They are not the same because transcript length includes the untranslated regions (UTRs) at both ends, which do not code for protein. ENST00000644072 encodes the same 624-amino-acid protein as the MANE transcript but carries much longer UTRs. The longest protein comes from a transcript that includes extra *coding* exon sequence.

*Checked 2026-10-23, Ensembl gene ENSG00000113163.20.*
:::

Switch back to the **Transcripts** view and click the ID of the longest transcript (by base pairs) to open its details.

:::{exercise} Question 4
:label: db-c2a-a3-q4
:nonumber:
How many coding exons does this transcript have, out of how many exons in total? How are exons and untranslated regions displayed?
:::

:::{solution} db-c2a-a3-q4
:class: dropdown
17 coding exons out of 18 exons in total ("Coding exons 17 of 18"). In the diagram, exons are drawn as boxes connected by lines (the introns). Coding parts are filled boxes, and untranslated regions are drawn as empty (outlined) boxes. One exon of this transcript, and part of another, is untranslated, which is where its extra length comes from (question 3).

*Checked 2026-10-23, Ensembl gene ENSG00000113163.20.*
:::

:::{exercise} Question 5
:label: db-c2a-a3-q5
:nonumber:
Look up the variant with the dbSNP identifier you found in assignment 2, question 5, in Ensembl: type the rs number into the search box at <https://www.ensembl.org/search> and open it in the Feature explorer. What is its consequence on the MANE Select transcript (protein-truncating or missense)? Does Ensembl tell you whether it is pathogenic? Where do you find that instead?
:::

:::{solution} db-c2a-a3-q5
:class: dropdown
rs1064794019 has two alternative alleles. The one OMIM describes is a **missense** variant on the MANE Select transcript ENST00000643780: serine to leucine at protein position 132 (position 395 of the coding sequence, in coding exon 4 of 17). The header bar nevertheless says "Most severe consequence: stop_gained": that refers to the *other* allele at the same position, a reminder to always check which allele you are looking at.

Ensembl shows no clinical interpretation (Variant phenotypes: 0). Whether the variant is pathogenic you find in ClinVar, via dbSNP, where it is currently classified as *conflicting*.

```{figure} figures/cu2a-ens-var.png
:name: db-fig-cu2a-ens-var
:alt: Ensembl, rs1064794019 transcript consequences.

Ensembl, rs1064794019 transcript consequences. Screenshot of Ensembl, 2026-10-28 (EMBL-EBI, reused with attribution under Ensembl's image reuse terms).
```

*Checked 2026-10-23, Ensembl (Release 2026-07; variant data from dbSNP 157).*
:::

## Assignment 4: Genetic and functional information on CERT1 in NCBI

Look up the human CERT1 gene in NCBI.

:::{exercise} Question 1
:label: db-c2a-a4-q1
:nonumber:
What is the NCBI Gene identifier of this gene and what are all of the names of this gene, besides the official HGNC name CERT1? Compare the synonyms to Ensembl and OMIM. Why is harmonization important?
:::

:::{solution} db-c2a-a4-q1
:class: dropdown
NCBI Gene ID **10087**. Other names (aliases): CERT, CERTL, COL4A3BP, GPBP, MRD34, NEDHSF, STARD11; the protein is also called *ceramide transfer protein* and *Goodpasture antigen-binding protein*. Ensembl lists CERT, COL4A3BP, GPBP and STARD11. NCBI adds disease abbreviations (MRD34, NEDHSF), which are names of the *disorder*, not of the gene.

Harmonisation matters because the same gene goes by many names (COL4A3BP was its official symbol until recently): searching literature or databases with only one name misses information, and different genes can share a name. Stable identifiers (NCBI Gene ID, Ensembl ID, HGNC ID) remove this ambiguity.

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 2
:label: db-c2a-a4-q2
:nonumber:
Give the RefSeq identifiers (NG\_, NM\_, NP\_) and names of the mRNA and protein for one of its splice variants.
:::

:::{solution} db-c2a-a4-q2
:class: dropdown
Genomic: **NG_029492.2**. Many transcript variants are acceptable; for example the MANE Select transcript **NM_001379029.1** (transcript variant 7) with protein **NP_001365958.1**, *ceramide transfer protein* (624 amino acids). Another example: NM_001130105.1 → NP_001123577.1 (*ceramide transfer protein isoform 3*, 752 amino acids, the longest isoform).

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 3
:label: db-c2a-a4-q3
:nonumber:
What is the chromosomal position of this gene?
:::

:::{solution} db-c2a-a4-q3
:class: dropdown
Chromosome 5, band 5q13.3: 75,368,486–75,511,981 on GRCh38, minus (reverse) strand.

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 4
:label: db-c2a-a4-q4
:nonumber:
How many exons does the gene have (total regardless of transcript)? Why is this a different number of exons when compared to the transcript you looked at in Ensembl?
:::

:::{solution} db-c2a-a4-q4
:class: dropdown
**20** exons for the gene. One transcript never uses all of them: alternative transcripts use different first exons and include or skip different exons, and the gene's count is the *union* of all exons used by any transcript. The MANE Select transcript has 17 exons, and the transcript you opened in Ensembl 18.

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 5
:label: db-c2a-a4-q5
:nonumber:
In which tissue is this gene expressed most (RNA sequencing of total RNA from 20 human tissues)?
:::

:::{solution} db-c2a-a4-q5
:class: dropdown
Thyroid (about 4.9 TPM), only just ahead of cerebellum (4.3). Expression is low and broad, so "brain/cerebellum" next to thyroid is a reasonable reading as well.

```{figure} figures/cu2a-ncbi-expression.png
:name: db-fig-cu2a-ncbi-expression
:alt: NCBI Gene CERT1, expression in 20 tissues.

NCBI Gene CERT1, expression in 20 tissues. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 6
:label: db-c2a-a4-q6
:nonumber:
To which neurological Phenotype is CERT1 associated? What is the OMIM identifier?
:::

:::{solution} db-c2a-a4-q6
:class: dropdown
The neurodevelopmental disorder of assignment 2: *neurodevelopmental disorder with hypotonia, speech delay, and dysmorphic facies* (formerly intellectual developmental disorder, autosomal dominant 34), OMIM **616351**.

*Checked 2026-10-23, NCBI Gene (annotation RS_2025_08).*
:::

:::{exercise} Question 7
:label: db-c2a-a4-q7
:nonumber:
Give one GO biological process annotation (name and GO ID) with IDA evidence. What does IDA mean and why is it considered strong evidence?
:::

:::{solution} db-c2a-a4-q7
:class: dropdown
For example *ER to Golgi ceramide transport*, GO:0035621 (others with IDA: intermembrane sphingolipid transfer GO:0120012, ceramide metabolic process GO:0006672, sphingomyelin biosynthetic process GO:0006686). IDA = *Inferred from Direct Assay*: the process was shown in a laboratory experiment directly for this protein, rather than inferred from sequence similarity or by a computer, which is why it counts as strong evidence.

*Checked 2026-10-23, UniProt release 2026_03.*
:::
