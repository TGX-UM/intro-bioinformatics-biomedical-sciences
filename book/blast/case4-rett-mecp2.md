(blast-case4)=
# Case 4: A gene behind Rett syndrome (BLASTn)

*Time: 10 min.*

:::{note}
Answers checked against NCBI on 2026-10-07. NCBI updates its databases and software, so your
numbers may differ slightly.
:::

Gert, a young patient, has just been diagnosed with a rare genetic disorder: **Rett syndrome**.
The medical team suspects a mutation in a particular gene. You isolate the patient's DNA, amplify
the suspected gene by PCR, and sequence the PCR product.

Your task is to identify the gene from this sequence and describe the mutation. You will also
find out more about the disease.

*Background: [Comparing sequences](background/comparing-sequences.md) (nucleotide alignment to
study DNA polymorphisms), [Which BLAST to use](background/which-blast.md) and
[Interpreting BLAST output](background/blast-output.md).*

The patient's sequence (1820 nucleotides,
{download}`download as FASTA <data/case4_patient_sequence.fasta>`):

```{literalinclude} data/case4_patient_sequence.fasta
:language: text
```

## Assignment: Identify the unknown gene

:::{tip}
If you did Case 3 first, the BLAST form may still be set to the 16S rRNA database. Set the
database back to **Standard databases** before you start.
:::

:::{exercise} Question 1
:label: blast-c4-q1
:nonumber:
Use **BLASTn** (choose **blastn** under **Program selection**, not megablast) to compare the
sequence with the default database. Describe the best hit for *Homo sapiens* and fill in its
metrics.

| Gene symbol | | | |
|---|---|---|---|
| **Query length** | | | |
| **Max score** | | **E-value** | |
| **Total score** | | **Percentage identity** | |
| **Query coverage** | | **Accession length** | |
:::

:::{solution} blast-c4-q1
:class: dropdown
The best hit is the RefSeq genomic region of the **MECP2** gene (NG_007107).

| Gene symbol | MECP2 | | |
|---|---|---|---|
| **Query length** | 1820 | | |
| **Max score** | 3278 | **E-value** | 0.0 |
| **Total score** | 3278 | **Percentage identity** | 99.95% |
| **Query coverage** | 100% | **Accession length** | 122,531 |

```{figure} figures/case4-blastn-descriptions.png
:name: blast-c4-descriptions
:alt: BLASTn results table. The top human hit is the MECP2 RefSeqGene NG_007107 with 100% query cover and 99.95% identity.

BLASTn results for the patient sequence. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 2
:label: blast-c4-q2
:nonumber:
What type of mutation is present in the patient's sequence? Where in the gene is the mismatch?

*Hint: in the **Alignments** tab, tick **CDS feature** to show the protein translation alongside
the alignment.*

*Compare with Assignment 1 of [Part 1](part1-pairwise-alignment.md), where you described the
same kinds of mutation by hand.*
:::

:::{solution} blast-c4-q2
:class: dropdown
A single point mutation: there are no gaps and the query coverage is 100%, with one mismatch in
1820 nucleotides.

In the alignment with NG_007107 the mismatch is in the **ATG start codon of exon 1**. In the
MECP2_e1 transcript (NM_001110792) this is **c.1A>T**: the codon ATG (methionine) becomes TTG
(leucine), p.(Met1Leu). With **CDS feature** ticked, you see the subject's M against the query's
L.

```{figure} figures/case4-alignment-cds-start-codon.png
:name: blast-c4-alignment
:alt: Alignment of the patient sequence with NG_007107 with the CDS feature shown. At the exon 1 start codon the reference has ATG (M) and the patient has TTG (L).

The mismatch at the exon 1 start codon, with the CDS translation shown. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 3
:label: blast-c4-q3
:nonumber:
How could this change affect the function of the gene and lead to Rett syndrome?

*Hint: click the accession number (NG_…) for a summary, or look up the gene in NCBI Gene
([ncbi.nlm.nih.gov/gene](https://www.ncbi.nlm.nih.gov/gene/)).*
:::

:::{solution} blast-c4-q3
:class: dropdown
MeCP2 exists as two isoforms. **MeCP2_e1** starts in exon 1 and is the main isoform in the brain;
**MeCP2_e2** starts in exon 2. Losing the exon 1 start codon stops MeCP2_e1 from being made, while
MeCP2_e2 is unaffected. This variant is listed in ClinVar
([VCV000156661](https://www.ncbi.nlm.nih.gov/clinvar/variation/156661/)) as *likely pathogenic*
for Rett syndrome, classified by the ClinGen expert panel.

**Background on MeCP2.** DNA methylation is the main chemical modification of eukaryotic genomes
and is essential for mammalian development. The human proteins MECP2, MBD1, MBD2, MBD3 and MBD4
form a family of nuclear proteins that share a methyl-CpG binding domain (MBD). All of them
except MBD3 bind specifically to methylated DNA, and MECP2, MBD1 and MBD2 can also repress
transcription from methylated gene promoters. Unlike the other family members, MECP2 is on the X
chromosome and subject to X inactivation. It is not needed in stem cells but is essential for
embryonic development. Mutations in MECP2 cause most cases of Rett syndrome, a progressive
neurodevelopmental disorder and one of the most common causes of cognitive disability in girls
and women. Loss-of-function mutations disrupt neuronal maturation and synaptic regulation, which
leads to the symptoms of Rett syndrome.

```{figure} figures/case4-mecp2-gene-summary.png
:name: blast-c4-gene
:alt: NCBI Gene summary page for human MECP2.

The NCBI Gene summary of MECP2. Screenshot of NCBI Gene, 2026-10-07 (NCBI, public domain).
```
:::

## Further reading

The OMIM entry on MECP2 lists the mutations linked to each phenotype:
[omim.org/entry/300005](https://www.omim.org/entry/300005).
