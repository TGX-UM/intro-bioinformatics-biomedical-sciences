(blast-case3)=
# Case 3: Identifying a food-borne pathogen (BLASTn)

*Time: 20 min.*

:::{note}
Answers checked against NCBI on 2026-10-07. NCBI updates its databases and software, so your
numbers may differ slightly.
:::

One sunny summer day, Samson came back to Maastricht from his holiday with stomach problems,
probably from food that had not been prepared properly. His doctor collected a stool sample, but
the standard tests could not show which microorganism was making him ill. So the laboratory
turned to genetics and sequenced bacterial ribosomal DNA from the sample.

A common way to identify bacteria is to sequence their **16S rRNA gene**. This gene is present in
all bacteria and highly conserved, which makes it useful as a "molecular clock" for tracing their
evolutionary relationships. It encodes part of the ribosome, which every cell needs for protein
synthesis. PCR with primers specific for this gene amplifies a region of it, which is then
sequenced. The result is a FASTA file with the 16S rRNA gene sequence.

The sequence that came back from the lab (106 nucleotides,
{download}`download as FASTA <data/case3_16S_rRNA.fasta>`):

```{literalinclude} data/case3_16S_rRNA.fasta
:language: text
```

## Assignment: Identify the unknown microorganism

:::{exercise} Question 1
:label: blast-c3-q1
:nonumber:
Run a nucleotide BLAST (BLASTn) of this sequence against the NCBI database of 16S ribosomal RNA
sequences: under **Database**, choose **rRNA/ITS databases** and then **16S ribosomal RNA
sequences (Bacteria and Archaea)** ({numref}`blast-c3-database`). Under **Program selection**,
choose **blastn** rather than megablast.

Which bacterial species is most similar to your sequence (ranked by E-value)? What is the
percentage identity?
:::

```{figure} figures/case3-16s-database-selection.png
:name: blast-c3-database
:alt: The database section of the BLASTn form, with rRNA/ITS databases selected and the 16S ribosomal RNA database chosen.

Selecting the 16S rRNA database in the BLASTn form. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```

:::{solution} blast-c3-q1
:class: dropdown
- Species at the top of the list: *Staphylococcus debuckii*
- Percentage identity of the best alignment: 97.20%

But look closer: **65 of the 100 hits have exactly the same score** (173 bits). *S. debuckii* is
listed first only because of how ties are ordered, so its position means nothing. This short
region of the 16S gene identifies the **genus**, not the species.

```{figure} figures/case3-results-descriptions.png
:name: blast-c3-descriptions
:alt: BLASTn results table against the 16S rRNA database. Many Staphylococcus species have the same max score of 173 and the same identity.

BLASTn results against 16S rRNA sequences. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 2
:label: blast-c3-q2
:nonumber:
Fill in the table for the best alignment.

| Max score | | **Query coverage** | |
|---|---|---|---|
| **Total score** | | **E-value** | |
:::

:::{solution} blast-c3-q2
:class: dropdown
| Max score | 173 | **Query coverage** | 100% |
|---|---|---|---|
| **Total score** | 173 | **E-value** | 4e-43 |

These values are for the **blastn** program, not megablast.
:::

:::{exercise} Question 3
:label: blast-c3-q3
:nonumber:
What do the total score and the max score mean?

*Background: [Interpreting BLAST output](background/blast-output.md).*
:::

:::{solution} blast-c3-q3
:class: dropdown
BLAST makes local alignments, so the alignment between the query and one hit can consist of
several sub-alignments. The **total score** adds up the scores of all of them; the **max score**
is the score of the best one only. Here there is only one sub-alignment, so both are 173.
:::

:::{exercise} Question 4
:label: blast-c3-q4
:nonumber:
How many gaps are there in the best alignment? Would you still call the two sequences similar?
:::

:::{solution} blast-c3-q4
:class: dropdown
There are 2 gaps, which is only about 1% of the sequence length. The sequences are very similar.

```{figure} figures/case3-top-alignment.png
:name: blast-c3-alignment
:alt: Pairwise alignment of the query with the top 16S hit, showing 97% identity and 2 gaps.

The best alignment. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 5
:label: blast-c3-q5
:nonumber:
Open the **Taxonomy** tab of the results and look at the lineage of the hits. To which genus do
the bacteria belong? Which species has the most hits?
:::

:::{solution} blast-c3-q5
:class: dropdown
They belong to the genus ***Staphylococcus***. *Staphylococcus aureus* has the most hits (5).

```{figure} figures/case3-taxonomy-lineage.png
:name: blast-c3-taxonomy
:alt: The Taxonomy tab of the BLAST results, with the lineage of the hits and the genus Staphylococcus.

The taxonomy lineage of the hits. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

## Further reading

A study that uses 16S rRNA sequencing to identify pathogens: {cite:t}`chen2014`.
