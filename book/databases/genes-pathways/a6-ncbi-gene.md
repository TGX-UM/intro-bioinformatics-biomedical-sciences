(db-p1-a6)=
# Assignment 6: Genetic and functional information on your gene from NCBI

*Time: 30 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

This assignment comes in three versions (A, B and C); see the version table on the practical page ({ref}`db-p1-versions`).

*Background: the [Reference guide](../guide/index.md) has one page per database.*

We continue with a database with more details on genes and their function: **NCBI Gene**, at the National Center for Biotechnology Information. Open the NCBI Gene page of your version's gene (see the table above). Version A can also reach it through the link on WikiPathways.

NCBI Gene integrates information from a wide range of species. A record on a gene may include nomenclature, Reference Sequences (RefSeqs), maps, pathways, variations, phenotypes, and links to genome-, phenotype-, and locus-specific resources worldwide.

:::{exercise} Question 1
:label: db-p1a6-q1
:nonumber:
What is the NCBI Gene identifier, official symbol and full name of your gene?
:::

:::{solution} db-p1a6-q1
:class: dropdown
- **A:** 3479, IGF1, *insulin like growth factor 1*.
- **B:** 2660, MSTN, *myostatin*.
- **C:** 2261, FGFR3, *fibroblast growth factor receptor 3*.

*Checked 2026-10-23, NCBI Gene.*
:::

:::{exercise} Question 2
:label: db-p1a6-q2
:nonumber:
What are other names (aliases) of this gene? Compare them with the synonyms Ensembl lists. Version A: compare with [assignment 3](a3-ensembl.md), question 1. Versions B and C: open the gene in Ensembl ([MSTN](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000138379), [FGFR3](https://www.ensembl.org/feature-explorer/GCA_000001405.29/gene:ENSG00000068078)). Are there differences? How could differences in names affect your searches in other databases, and how do databases try to limit this problem?
:::

:::{solution} db-p1a6-q2
:class: dropdown
- **A — IGF1:** NCBI: IGF, IGF-I, IGFI, MGF. Ensembl: IGF, IGF-I, IGF1A, IGFI.
- **B — MSTN:** NCBI: GDF8, MSLHP. Ensembl: GDF8. UniProt even uses GDF8 as the main name ("Growth/differentiation factor 8").
- **C — FGFR3:** NCBI: ACH, CD333, CEK2, HSFGFR3EX, JTK4. Ensembl: ACH, CD333, CEK2, JTK4.

The lists overlap but are not identical, and formatting differs (IGF-I vs IGFI). Using alternative names inconsistently can lead to missed literature, wrong search results, or confusion between genes or species. Databases limit this by providing synonym lists, using stable identifiers (NCBI Gene IDs, Ensembl IDs, HGNC IDs) and cross-linking to each other. Stable identifiers remove the ambiguity, which is why they are essential in bioinformatics.

*Checked 2026-10-23, NCBI Gene and Ensembl.*
:::

:::{exercise} Question 3
:label: db-p1a6-q3
:nonumber:
On which chromosome is your gene located? How many exons does the gene have (total, regardless of transcript)?
:::

:::{solution} db-p1a6-q3
:class: dropdown
- **A — IGF1:** chromosome 12 (12q23.2); 7 exons.
- **B — MSTN:** chromosome 2 (2q32.2); 3 exons.
- **C — FGFR3:** chromosome 4 (4p16.3); 19 exons.

*Checked 2026-10-23, NCBI Gene.*
:::

:::{exercise} Question 4
:label: db-p1a6-q4
:nonumber:
Explain what RefSeq identifiers are, and name the main categories relevant for genes, transcripts and proteins. (Start with <https://en.wikipedia.org/wiki/RefSeq>.)
:::

:::{solution} db-p1a6-q4
:class: dropdown
The Reference Sequence (RefSeq) database is an open-access, annotated and curated collection of nucleotide sequences (DNA, RNA) and their protein products. It aims to provide one record for each natural biological molecule (DNA, RNA or protein) for major organisms, with separate but linked records for the genomic DNA, the transcripts and the proteins.

The prefix tells you the type of record:

- **NG\_**: genomic region of a gene (RefSeqGene).
- **NC\_**: complete chromosome.
- **NM\_**: messenger RNA (curated).
- **NR\_**: non-coding RNA (curated), not translated into protein.
- **NP\_**: protein (curated).
- **XM\_** / **XP\_**: predicted (model) mRNA and protein, made by computational annotation and not yet curated.
:::

:::{exercise} Question 5
:label: db-p1a6-q5
:nonumber:
Give the RefSeq identifier of the gene (NG\_), and the RefSeq IDs of the **MANE Select** transcript (NM\_) and its protein (NP\_). What is the name of that protein? (Hint: use the table of contents to go to the *NCBI Reference Sequences (RefSeq)* section. The classic gene page does not label which transcript is MANE Select; find out via the **Try the new Transcript table** link, or via the RefSeq match column of the Ensembl *Transcripts table*.)

Genomic RefSeq ID:

mRNA RefSeq ID:

Protein RefSeq ID:

Protein name:
:::

:::{solution} db-p1a6-q5
:class: dropdown
| | A — IGF1 | B — MSTN | C — FGFR3 |
|---|---|---|---|
| Genomic (NG\_) | NG_011713.1 | NG_009800.1 | NG_012632.1 |
| mRNA, MANE Select (NM\_) | NM_000618.5 | NM_005259.3 | NM_000142.5 |
| Protein (NP\_) | NP_000609.1 | NP_005250.1 | NP_000133.1 |
| Protein name | insulin-like growth factor 1 isoform 4 preproprotein | growth/differentiation factor 8 preproprotein | fibroblast growth factor receptor 3 isoform 1 precursor |

The MANE Select transcript is the same one Ensembl flags as MANE Select ([assignment 3](a3-ensembl.md)). Note that for IGF1 this protein has 153 amino acids, while UniProt's canonical IGF1 sequence has 195. Different databases choose different reference forms.

```{figure} ../figures/2a-train-A-ncbi-refseq.png
:name: db-fig-2a-train-A-ncbi-refseq
:alt: Version A: NCBI Gene IGF1, RefSeq section.

Version A: NCBI Gene IGF1, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2a-train-B-ncbi-refseq.png
:name: db-fig-2a-train-B-ncbi-refseq
:alt: Version B: NCBI Gene MSTN, RefSeq section.

Version B: NCBI Gene MSTN, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2a-train-C-ncbi-refseq.png
:name: db-fig-2a-train-C-ncbi-refseq
:alt: Version C: NCBI Gene FGFR3, RefSeq section.

Version C: NCBI Gene FGFR3, RefSeq section. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

*Checked 2026-10-24, NCBI RefSeq (annotation RS_2025_08).*
:::

:::{exercise} Question 6
:label: db-p1a6-q6
:nonumber:
How many transcripts (splice variants) are listed in the RefSeq section for your gene? How many are curated (NM\_ / NR\_) and how many predicted (XM\_)? (The RefSeq section lists the transcripts directly. The **Try the new Transcript table** link at the top of that section leaves NCBI Gene for the NCBI Datasets page, which counts differently. Answer from the RefSeq section itself, and say which route you used.)
:::

:::{solution} db-p1a6-q6
:class: dropdown
- **A — IGF1:** 7 curated NM\_ and 3 predicted XM\_ on the reference genome GRCh38.
- **B — MSTN:** 1: a single curated NM\_, no predicted ones.
- **C — FGFR3:** 5 curated NM\_ and 1 curated NR\_ (non-coding), plus 12 predicted XM\_ on GRCh38 (for 10 predicted isoforms, X1–X10; some isoforms are encoded by two XM\_ records).

Careful: the predicted models are listed once for each genome assembly NCBI annotates (the reference GRCh38 and the newer, complete T2T-CHM13 genome), so a page may show each XM\_ model twice (for IGF1: 6 instead of 3). Both counts are acceptable if you say what you counted.

⚠️ **Route-dependent and release-volatile.** The *Try the new Transcript table* link leaves NCBI Gene for NCBI Datasets, which counts differently. Both are defensible; say which page you read it from. The number of predicted XM\_ models in particular changes with each annotation release.

*Checked 2026-10-24, NCBI RefSeq annotation RS_2025_08.*
:::

:::{exercise} Question 7
:label: db-p1a6-q7
:nonumber:
Go to the **Expression** section and select the **adult** dataset in the drop-down at the top of the section (HPA RNA-seq normal tissues). In which tissues is your gene expressed most (top 2)? Is that what you would expect from its function?
:::

:::{solution} db-p1a6-q7
:class: dropdown
- **A — IGF1:** endometrium and fat (then prostate and liver). Most circulating IGF-1 is made by the liver in response to growth hormone, but IGF-1 also acts locally, in many tissues.
- **B — MSTN:** oesophagus and brain, but all values are very low (below 1 TPM). The tissue where myostatin matters most, **skeletal muscle**, is *not among the 27 tissues* in this dataset. An expression chart can only show the tissues that were sampled: no signal is not the same as no expression.
- **C — FGFR3:** skin, by far (about 120 TPM), then oesophagus and brain. Cartilage and the growth plate, where FGFR3 controls bone growth, are not in the dataset.

⚠️ **Release-volatile.** *Checked 2026-10-23, NCBI Gene, HPA RNA-seq normal tissues (PRJEB4337).*

```{figure} ../figures/2a-train-A-ncbi-expression.png
:name: db-fig-2a-train-A-ncbi-expression
:alt: Version A: NCBI Gene IGF1, adult expression.

Version A: NCBI Gene IGF1, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2a-train-B-ncbi-expression.png
:name: db-fig-2a-train-B-ncbi-expression
:alt: Version B: NCBI Gene MSTN, adult expression.

Version B: NCBI Gene MSTN, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```

```{figure} ../figures/2a-train-C-ncbi-expression.png
:name: db-fig-2a-train-C-ncbi-expression
:alt: Version C: NCBI Gene FGFR3, adult expression.

Version C: NCBI Gene FGFR3, adult expression. Screenshot of NCBI Gene, 2026-10-23 (NCBI, public domain).
```
:::

:::{exercise} Question 8
:label: db-p1a6-q8
:nonumber:
Now switch the drop-down to the **fetal** dataset (this is the one the section may open on by default). In which organ is your gene expressed most during human fetal development?
:::

:::{solution} db-p1a6-q8
:class: dropdown
- **A — IGF1:** lung (week 10). IGF1 is important for lung maturation and branching morphogenesis.
- **B — MSTN:** adrenal gland (week 10), but again at trace level; the fetal dataset has no skeletal muscle either.
- **C — FGFR3:** lung and intestine (weeks 15–20).

*Checked 2026-10-23, NCBI Gene, fetal tissue RNA-seq (PRJNA270632).*
:::

:::{exercise} Question 9
:label: db-p1a6-q9
:nonumber:
Scroll down to the **Phenotypes** section. Which phenotype(s) are associated with your gene? Is this what you would expect from its function? What is the OMIM ID of the main phenotype?
:::

:::{solution} db-p1a6-q9
:class: dropdown
- **A — IGF1:** growth delay due to insulin-like growth factor I deficiency, OMIM 608747. Expected: IGF1 is essential for normal linear growth and skeletal development.
- **B — MSTN:** muscle hypertrophy, OMIM 614160 (autosomal recessive). OMIM marks it "?Muscle hypertrophy": the question mark means the link between gene and phenotype is still provisional. Expected, because myostatin is a *negative* regulator of muscle growth: losing it gives more muscle. The same happens in "double-muscled" cattle breeds and in mice without myostatin.
- **C — FGFR3:** achondroplasia, OMIM 100800 (autosomal dominant), the most common form of dwarfism, plus related skeletal dysplasias (hypochondroplasia, thanatophoric dysplasia types I and II, SADDAN, Muenke and Crouzon syndrome with acanthosis nigricans) and several somatic cancers (bladder, cervical, colorectal). Expected, because FGFR3 *slows down* chondrocyte proliferation in the growth plate: activating mutations such as Gly380Arg make it overactive, and bone growth is reduced.

*Checked 2026-10-23, NCBI Gene and ClinVar; OMIM numbers checked by hand 2026-10-24.*
:::

:::{exercise} Question 10
:label: db-p1a6-q10
:nonumber:
Move to the **Pathways from PubChem** section. Which pathway databases are included in the list, and which one provides the most entries? Is a WikiPathways pathway you have used today included? If so, what is its identifier? (Hint: the widget is a small embedded panel; type `WP` plus the number into its own search box rather than scrolling.)
:::

:::{solution} db-p1a6-q10
:class: dropdown
The list combines Reactome and WikiPathways, plus PANTHER for IGF1 and the Pathway Interaction Database and PathBank for FGFR3; for all three genes most entries come from WikiPathways. Versions A and C will find WP3932 ([assignment 4](a4-pi3k-pathway.md)), because both IGF1 and FGFR3 are in it; version A also finds WP4194 (assignment 2). None of today's pathways contains MSTN, but version B will find WP3850 (*Factors and pathways affecting insulin-like growth factor (IGF1)-Akt signaling*), in which myostatin acts on IGF1-Akt signalling through its receptor ACVR2B. The number of pathways grows as pathway databases grow.

⚠️ **Release-volatile.** *Checked 2026-10-28, WikiPathways and PubChem pathway data; the PubChem widget itself to be re-checked.*
:::

:::{exercise} Question 11
:label: db-p1a6-q11
:nonumber:
**Compare with another version.** Put your answers to questions 6, 7 and 9 next to those of a classmate who chose a different version (or next to your own answers for a second version). Which gene has the most transcripts and which the fewest? Which phenotype comes from *too little* activity of the gene product, and which from *too much*?
:::

:::{solution} db-p1a6-q11
:class: dropdown
- **Transcripts:** MSTN has a single RefSeq transcript, IGF1 7 curated (plus predicted models) and FGFR3 6 curated (plus predicted models). In Ensembl: 2, 15 and 24. A small, simple gene versus genes with many alternative forms.
- **Too little:** IGF1 deficiency (loss of a growth *stimulator*, so less growth) and MSTN-related muscle hypertrophy (loss of a growth *inhibitor*, so more muscle).
- **Too much:** achondroplasia. An activating FGFR3 mutation over-activates a growth *inhibitor*, so less bone growth.

Together they show that growth is set by a balance of stimulating and inhibiting signals, and that a mutation's effect depends on whether it removes or enhances the function of the protein.
:::
