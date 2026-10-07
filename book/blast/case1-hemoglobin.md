(blast-case1)=
# Case 1: Hemoglobin α and β subunits (BLASTp)

*Time: 30 min.*

:::{note}
Answers checked against NCBI on 2026-10-07. NCBI updates its databases and software, so your
numbers may differ slightly.
:::

The α and β subunits of hemoglobin, the oxygen-carrying protein in red blood cells, descend from
one ancestral protein that was duplicated in evolution. In this case you compare the human α and β
hemoglobin proteins and use them to explore pairwise sequence alignment with BLAST.

:::{exercise} Question 1
:label: blast-c1-q1
:nonumber:
Go to NCBI Protein ([ncbi.nlm.nih.gov/protein](https://www.ncbi.nlm.nih.gov/protein)). The RefSeq
identifier of human hemoglobin subunit α is NP_000508. Use the search bar to find the RefSeq
identifier of human hemoglobin subunit β. How many amino acids does each subunit have?
:::

:::{solution} blast-c1-q1
:class: dropdown
Subunit β is **NP_000509**.

The "NP" prefix tells you the record is a protein. NCBI has several databases, among them RefSeq,
Gene and Protein. Looking up a protein sequence is easiest in NCBI Protein:
[ncbi.nlm.nih.gov/protein/NP_000509](https://www.ncbi.nlm.nih.gov/protein/NP_000509). The FASTA
link is at the top of the record ({numref}`blast-c1-record`).

Lengths:
- NP_000508 (α): 142 amino acids
- NP_000509 (β): 147 amino acids

```{figure} figures/case1-np000509-protein-record.png
:name: blast-c1-record
:alt: NCBI Protein record for NP_000509, hemoglobin subunit beta, with the FASTA link at the top of the page.

The NCBI Protein record of NP_000509. Screenshot of NCBI Protein, 2026-10-07 (NCBI, public domain).
```
:::

:::{exercise} Question 2
:label: blast-c1-q2
:nonumber:
Open the RefSeq records of both proteins and click **FASTA** at the top of the page. This shows
the sequence in FASTA format. What does the FASTA format look like in general?
:::

:::{solution} blast-c1-q2
:class: dropdown
A FASTA record starts with a greater-than sign (`>`) followed by a description of the sequence,
all on one line. The lines after it hold the sequence itself, one letter per amino acid or
nucleotide.

```text
>NP_000508.1 hemoglobin subunit alpha [Homo sapiens]
MVLSPADKTNVKAAWGKVGAHAGEYGAEALERMFLSFPTTKTYFPHFDLSHGSAQVKGHGKKVADALTNA
VAHVDDMPNALSALSDLHAHKLRVDPVNFKLLSHCLLVTLAAHLPAEFTPAVHASLDKFLASVSTVLTSK
YR
```

```text
>NP_000509.1 hemoglobin subunit beta [Homo sapiens]
MVHLTPEEKSAVTALWGKVNVDEVGGEALGRLLVVYPWTQRFFESFGDLSTPDAVMGNPKVKAHGKKVLG
AFSDGLAHLDNLKGTFATLSELHCDKLHVDPENFRLLGNVLVCVLAHHFGKEFTPPVQAAYQKVVAGVAN
ALAHKYH
```
:::

Now use BLAST to compare the two subunits. Go to [blast.ncbi.nlm.nih.gov](https://blast.ncbi.nlm.nih.gov)
and choose **Protein BLAST** (BLASTp). To compare two sequences with each other, tick the checkbox
**Align two or more sequences** ({numref}`blast-c1-form`).

```{figure} figures/case1-align-two-sequences-form.png
:name: blast-c1-form
:alt: The BLASTp input form with the "Align two or more sequences" checkbox ticked, showing a query box and a subject box.

The BLASTp input form, with the checkbox for pairwise sequence comparison. Screenshot of NCBI BLAST, 2026-10-07 (NCBI, public domain).
```

:::{exercise} Question 3
:label: blast-c1-q3
:nonumber:
Align the α and β subunits with BLAST using the default settings and fill in the table.

*Tip: instead of copying the FASTA sequences, you can type the RefSeq identifiers into the BLAST
input boxes.*

| Query length | | | |
|---|---|---|---|
| **Max score** | | **E-value** | |
| **Total score** | | **Percentage identity** | |
| **Query coverage** | | **Accession length** | |
:::

:::{solution} blast-c1-q3
:class: dropdown
| Query length | 142 (α); the subject, β, is 147 | | |
|---|---|---|---|
| **Max score** | 114 | **E-value** | 2e-38 |
| **Total score** | 114 | **Percentage identity** | 43.45% |
| **Query coverage** | 98% | **Accession length** | 147 |
:::

:::{exercise} Question 4
:label: blast-c1-q4
:nonumber:
Click the **Alignments** tab and fill in the table.

| Alignment length | | **Positives** | |
|---|---|---|---|
| **Identities** | | **Gaps** | |
:::

:::{solution} blast-c1-q4
:class: dropdown
| Alignment length | 145 | **Positives** | 88/145 (61%) |
|---|---|---|---|
| **Identities** | 63/145 (43%) | **Gaps** | 8/145 (6%) |

Notes:
- The alignment length is not necessarily the length of the query or the hit. Here it is 145, the
  denominator in the fractions.
- *Positives* is BLAST's term for what is also called *similarity*.
:::

:::{exercise} Question 5
:label: blast-c1-q5
:nonumber:
Based on your findings in question 4, are the sequences very similar?
:::

:::{solution} blast-c1-q5
:class: dropdown
They are moderately similar (about 43% identity). That fits a common ancestor followed by
divergence into proteins with different roles.
:::

:::{exercise} Question 6
:label: blast-c1-q6
:nonumber:
Go back to the BLASTp page. You will now explore how the scoring matrix affects the alignment. By
default BLAST uses the BLOSUM62 matrix. Click **+ Algorithm parameters** at the bottom of the
input form and change the matrix. Changing the matrix also changes the default gap penalties
(**Gap Costs**). Fill in the table with the default gap costs for each matrix.

| Matrix | Gap existence | Gap extension |
|---|---|---|
| BLOSUM62 | | |
| BLOSUM45 | | |
| PAM70 | | |
| PAM250 | | |
:::

:::{solution} blast-c1-q6
:class: dropdown
| Matrix | Gap existence | Gap extension |
|---|---|---|
| BLOSUM62 | 11 | 1 |
| BLOSUM45 | 14 | 2 |
| PAM70 | 10 | 1 |
| PAM250 | 15 | 2 |

*Existence* is BLAST's term for what is also called gap *opening*.
:::

:::{exercise} Question 7
:label: blast-c1-q7
:nonumber:
Repeat the run of question 3 with BLOSUM45 (and its default gap costs) and fill in both tables
again.

| Query length | | | |
|---|---|---|---|
| **Max score** | | **E-value** | |
| **Total score** | | **Percentage identity** | |
| **Query coverage** | | **Accession length** | |

| Alignment length | | **Positives** | |
|---|---|---|---|
| **Identities** | | **Gaps** | |
:::

:::{solution} blast-c1-q7
:class: dropdown
| Query length | 142 | | |
|---|---|---|---|
| **Max score** | 113 | **E-value** | 8e-39 |
| **Total score** | 113 | **Percentage identity** | 43.45% |
| **Query coverage** | 98% | **Accession length** | 147 |

| Alignment length | 145 | **Positives** | 92/145 (63%) |
|---|---|---|---|
| **Identities** | 63/145 (43%) | **Gaps** | 8/145 (6%) |
:::

:::{exercise} Question 8
:label: blast-c1-q8
:nonumber:
The score in question 7 differs from the score in question 3. Can you compare these scores? Does
the alignment with the highest score have the best alignment?
:::

:::{solution} blast-c1-q8
:class: dropdown
No. You can only compare raw scores of two alignments directly if both the input sequences and
all algorithm settings (matrix, gap penalties and so on) are the same. Raw scores cannot be
compared across matrices. Bit scores and E-values are normalised, so they can be compared
roughly.
:::

:::{exercise} Question 9
:label: blast-c1-q9
:nonumber:
Apart from the score, what else differs between the results of questions 3–4 and question 7? How
can you explain this?
:::

:::{solution} blast-c1-q9
:class: dropdown
The similarity (positives) is higher with BLOSUM45 (63%) than with BLOSUM62 (61%). BLOSUM45 is
built for more divergent sequences than BLOSUM62, so it counts somewhat more amino acid pairs as
similar.
:::
