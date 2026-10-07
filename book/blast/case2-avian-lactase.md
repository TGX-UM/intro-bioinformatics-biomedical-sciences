(blast-case2)=
# Case 2: An unknown chicken transcript (BLASTx)

*Time: 20 min.*

:::{note}
Answers checked against NCBI on 2026-10-07. NCBI updates its databases and software, so your
numbers may differ slightly.
:::

The chicken genome is not yet fully annotated. Comparing a chicken transcript with the proteins
of other birds can reveal which gene it comes from. The same comparison also says something about
how closely related the species are. In this case you compare an unknown chicken transcript with
the proteins of the turkey and the swan goose.

*Background: [Comparing sequences](background/comparing-sequences.md) (why protein comparisons
reach further back in evolution), [Which BLAST to use](background/which-blast.md) and
[Interpreting BLAST output](background/blast-output.md).*

The nucleotide sequence of the unknown transcript (1771 nucleotides,
{download}`download as FASTA <data/case2_unknown_transcript.fasta>`):

```{literalinclude} data/case2_unknown_transcript.fasta
:language: text
```

## Assignment: BLASTx against turkey and swan goose

BLASTx translates a nucleotide query in all six reading frames and searches the translations
against a protein database (see [Which BLAST to use](background/which-blast.md)). Comparing at the
protein level is the better choice across species, because many changes in the DNA do not change
the protein ([Comparing sequences](background/comparing-sequences.md)).

:::{exercise} Question 1
:label: blast-c2-q1
:nonumber:
Run BLASTx against the **common turkey (taxid 9103)**, with **Reference proteins
(refseq_protein)** as the database. Fill in the table for the best hit.

| Hit description | | | |
|---|---|---|---|
| **Query length** | | | |
| **Max score** | | **E-value** | |
| **Total score** | | **Percentage identity** | |
| **Query coverage** | | **Accession length** | |
:::

:::{solution} blast-c2-q1
:class: dropdown
| Hit description | lactase/phlorizin hydrolase [*Meleagris gallopavo*] | | |
|---|---|---|---|
| **Query length** | 1771 | | |
| **Max score** | 461 | **E-value** | 1e-144 |
| **Total score** | 2402 | **Percentage identity** | 95.02% |
| **Query coverage** | 100% | **Accession length** | 1919 |

```{figure} figures/case2-turkey-blastx-descriptions.png
:name: blast-c2-descriptions
:alt: BLASTx results table for the turkey search. The top hit is lactase/phlorizin hydrolase from Meleagris gallopavo.

BLASTx results against turkey RefSeq proteins. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 2
:label: blast-c2-q2
:nonumber:
Click the accession of the best hit, on the right of the results table. This takes you to its
RefSeq record. Which gene codes for this protein?
:::

:::{solution} blast-c2-q2
:class: dropdown
**LCT** (lactase). You can see this in the right-hand panel "More about the gene LCT", or by
clicking the RefSeq mRNA linked to this protein (XM_010714026).

```{figure} figures/case2-turkey-lph-protein-record.png
:name: blast-c2-record
:alt: NCBI Protein record of the turkey lactase/phlorizin hydrolase, with the gene LCT shown in the right-hand panel.

The RefSeq protein record of the turkey hit. Screenshot of NCBI Protein, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 3
:label: blast-c2-q3
:nonumber:
Open the **Alignments** tab of the results. Describe the top alignment. Why are there several
ranges for this one hit?
:::

:::{solution} blast-c2-q3
:class: dropdown
BLAST makes *local* alignments, so different parts of the query can match different regions of
the same database sequence. Each range is one of these local alignments, and each shows the
**Frame** of the query translation it uses.

These ranges are the *sub hits* described in [Interpreting BLAST output](background/blast-output.md).
They explain why the total score in question 1 (2402) is much higher than the max score (461):
the max score is the best range alone, the total score adds them all up.

Two things explain why this hit has so many ranges:

- Lactase/phlorizin hydrolase has four homologous repeat domains, so parts of the query match
  more than one of them. For example, query 1162–1770 matches subject 884–1086 at 97% identity and
  subject 361–563 at about 57%.
- The query switches reading frame, from +3 to +1, around nucleotides 725–733.

```{figure} figures/case2-turkey-alignment-ranges.png
:name: blast-c2-ranges
:alt: The top BLASTx alignment, split into several ranges, each with its own score, identity and reading frame.

The top alignment against the turkey protein, with its ranges and reading frames. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 4
:label: blast-c2-q4
:nonumber:
Run BLASTx against the **swan goose (taxid 8845)**, again with **Reference proteins
(refseq_protein)** as the database. Fill in the table for the best hit.

| Hit description | | | |
|---|---|---|---|
| **Query length** | | | |
| **Max score** | | **E-value** | |
| **Total score** | | **Percentage identity** | |
| **Query coverage** | | **Accession length** | |
:::

:::{solution} blast-c2-q4
:class: dropdown
| Hit description | lactase/phlorizin hydrolase [*Anser cygnoides*] | | |
|---|---|---|---|
| **Query length** | 1771 | | |
| **Max score** | 444 | **E-value** | 9e-139 |
| **Total score** | 2351 | **Percentage identity** | 91.29% |
| **Query coverage** | 100% | **Accession length** | 1926 |

*Anser cygnoides*, the swan goose, is a goose, not a swan.
:::

:::{exercise} Question 5
:label: blast-c2-q5
:nonumber:
What differences do you see between the best hits for turkey and swan goose? What could they
mean for the evolutionary distance between these birds and the chicken?
:::

:::{solution} blast-c2-q5
:class: dropdown
The percentage identity is lower for the swan goose (91.29%) than for the turkey (95.02%). This
points to a larger evolutionary distance between chicken and swan goose, while chicken and turkey
are more closely related. Both searches still find the same gene, LCT, as the best match, which
suggests that this gene is well conserved.
:::

## Further reading

A study that uses this type of approach: {cite:t}`orgeur2017`.
