(blast-part1)=
# Part 1: Pairwise sequence alignment

*Time: 30 min. Pen and paper, no computer needed. This part recaps the lecture.*

To illustrate, we align the following two DNA sequences with each other:

```text
Sequence A: ACCAGATCGTAGGACTGACGT
Sequence B: ACCACATCGGACTGACGT
```

This gives the following pairwise alignment, where `|` marks an identical base and `-` a gap:

```text
Sequence A  ACCAGATCGTAGGACTGACGT
            |||| ||||   |||||||||
Sequence B  ACCACATCG---GACTGACGT
```

## Assignment 1: DNA sequence comparison

:::{exercise} Question 1
:label: blast-p1-a1-q1
:nonumber:
Describe the sequence similarity. To what extent is sequence B identical to sequence A?
:::

:::{solution} blast-p1-a1-q1
:class: dropdown
- Identical: 17 out of 21 bases (81%).
- Gaps: one gap of 3 bases.
- Mismatches: 1.
:::

:::{exercise} Question 2
:label: blast-p1-a1-q2
:nonumber:
Describe the differences between the two sequences. What kind of mutations could have happened
here?

*Hint: you cannot know which of the two sequences is the one without the mutation.*
:::

:::{solution} blast-p1-a1-q2
:class: dropdown
- A point mutation of a single base (G>C or C>G).
- A deletion *or* an insertion of 3 bases, which is one codon.
:::

:::{exercise} Question 3
:label: blast-p1-a1-q3
:nonumber:
Describe what could happen to the function of the protein encoded by a DNA sequence with a
mutation.
:::

:::{solution} blast-p1-a1-q3
:class: dropdown
The protein can become less or more active, fold differently, or not be made as a functional
protein at all, for example when a nonsense mutation puts a STOP codon in the wrong place. A
mutation can also have no effect at all (a silent mutation).
:::

## Assignment 2: From DNA sequence to protein sequence

:::{exercise} Assignment 2
:label: blast-p1-a2
:nonumber:
1. Transcribe the two DNA sequences into RNA in the tables below. Assume that the given sequences
   are the *template* strands that are transcribed, and that the reading frame starts where the
   sequence starts.
2. Translate the two RNA sequences into amino acid (AA) sequences, starting at the first triplet.
   Use the codon wheel in {numref}`blast-codon-wheel` and write the one-letter code (for serine,
   write S, not Ser).

**Sequence A**

| DNA | A | C | C | A | G | A | T | C | G | T | A | G | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
| AA  |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |

**Sequence B**

| DNA | A | C | C | A | C | A | T | C | G | - | - | - | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
| AA  |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
:::

:::{solution} blast-p1-a2
:class: dropdown
The template strand is read as its complement (A→U, T→A, C→G, G→C).

**Sequence A**

| DNA | A | C | C | A | G | A | T | C | G | T | A | G | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA | U | G | G | U | C | U | A | G | C | A | U | C | C | U | G | A | C | U | G | C | A |
| AA  | **W** | | | **S** | | | **S** | | | **I** | | | **L** | | | **T** | | | **A** | | |

**Sequence B**

| DNA | A | C | C | A | C | A | T | C | G | - | - | - | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA | U | G | G | U | G | U | A | G | C | - | - | - | C | U | G | A | C | U | G | C | A |
| AA  | **W** | | | **C** | | | **S** | | | **-** | | | **L** | | | **T** | | | **A** | | |

So the protein sequences are `WSSILTA` (A) and `WCS-LTA` (B).
:::

```{figure} figures/codon-wheel.svg
:name: blast-codon-wheel
:width: 420px
:alt: Circular codon table. Read from the centre outwards: first base, second base, third base, then the amino acid. Start codon AUG (Met) and the stop codons UAA, UAG and UGA are marked.

The standard RNA codon table arranged as a wheel. Read from the centre (5′) outwards.
Image: [Mouagip, *Aminoacids table*](https://commons.wikimedia.org/wiki/File:Aminoacids_table.svg), Wikimedia Commons, public domain.
```

## Assignment 3: Choosing a scoring matrix for the protein sequences

:::{exercise} Question 1
:label: blast-p1-a3-q1
:nonumber:
If you use a PAM (Point Accepted Mutation) matrix, would you choose a high or a low number for
this comparison? Why?
:::

:::{solution} blast-p1-a3-q1
:class: dropdown
PAM numbers increase for comparisons of more divergent proteins. A low PAM (for example PAM30)
detects close homologues, and a high PAM (for example PAM250) detects distant ones. These
sequences are similar, so use a **low** PAM.
:::

:::{exercise} Question 2
:label: blast-p1-a3-q2
:nonumber:
What is the range of numbers for PAM matrices?
:::

:::{solution} blast-p1-a3-q2
:class: dropdown
In theory the scale runs from PAM1 to PAM500, but PAM30 to PAM250 are the most used.
:::

:::{exercise} Question 3
:label: blast-p1-a3-q3
:nonumber:
If you use a BLOSUM (BLOcks SUbstitution Matrix) matrix, would you choose a high or a low number
for this comparison? Why?
:::

:::{solution} blast-p1-a3-q3
:class: dropdown
BLOSUM works the other way round: lower-numbered matrices are for more divergent proteins, and
higher-numbered ones for closely related proteins {cite}`henikoff1992`. These sequences are
similar, so use a **high** BLOSUM.
:::

:::{exercise} Question 4
:label: blast-p1-a3-q4
:nonumber:
What is the range of numbers for BLOSUM matrices?
:::

:::{solution} blast-p1-a3-q4
:class: dropdown
BLOSUM matrices range roughly from BLOSUM30 to BLOSUM100.
:::

## Assignment 4: Scoring a protein alignment with BLOSUM80

The BLOSUM80 matrix gives a score for every pair of amino acids. Positive scores mean the pair is
seen more often than by chance in related proteins, negative scores less often.

```{code-block} text
:caption: BLOSUM80 substitution matrix (20 standard amino acids). Source: NCBI BLAST matrix file `BLOSUM80`, after Henikoff & Henikoff (1992).
    A  R  N  D  C  Q  E  G  H  I  L  K  M  F  P  S  T  W  Y  V
A   7 -3 -3 -3 -1 -2 -2  0 -3 -3 -3 -1 -2 -4 -1  2  0 -5 -4 -1
R  -3  9 -1 -3 -6  1 -1 -4  0 -5 -4  3 -3 -5 -3 -2 -2 -5 -4 -4
N  -3 -1  9  2 -5  0 -1 -1  1 -6 -6  0 -4 -6 -4  1  0 -7 -4 -5
D  -3 -3  2 10 -7 -1  2 -3 -2 -7 -7 -2 -6 -6 -3 -1 -2 -8 -6 -6
C  -1 -6 -5 -7 13 -5 -7 -6 -7 -2 -3 -6 -3 -4 -6 -2 -2 -5 -5 -2
Q  -2  1  0 -1 -5  9  3 -4  1 -5 -4  2 -1 -5 -3 -1 -1 -4 -3 -4
E  -2 -1 -1  2 -7  3  8 -4  0 -6 -6  1 -4 -6 -2 -1 -2 -6 -5 -4
G   0 -4 -1 -3 -6 -4 -4  9 -4 -7 -7 -3 -5 -6 -5 -1 -3 -6 -6 -6
H  -3  0  1 -2 -7  1  0 -4 12 -6 -5 -1 -4 -2 -4 -2 -3 -4  3 -5
I  -3 -5 -6 -7 -2 -5 -6 -7 -6  7  2 -5  2 -1 -5 -4 -2 -5 -3  4
L  -3 -4 -6 -7 -3 -4 -6 -7 -5  2  6 -4  3  0 -5 -4 -3 -4 -2  1
K  -1  3  0 -2 -6  2  1 -3 -1 -5 -4  8 -3 -5 -2 -1 -1 -6 -4 -4
M  -2 -3 -4 -6 -3 -1 -4 -5 -4  2  3 -3  9  0 -4 -3 -1 -3 -3  1
F  -4 -5 -6 -6 -4 -5 -6 -6 -2 -1  0 -5  0 10 -6 -4 -4  0  4 -2
P  -1 -3 -4 -3 -6 -3 -2 -5 -4 -5 -5 -2 -4 -6 12 -2 -3 -7 -6 -4
S   2 -2  1 -1 -2 -1 -1 -1 -2 -4 -4 -1 -3 -4 -2  7  2 -6 -3 -3
T   0 -2  0 -2 -2 -1 -2 -3 -3 -2 -3 -1 -1 -4 -3  2  8 -5 -3  0
W  -5 -5 -7 -8 -5 -4 -6 -6 -4 -5 -4 -6 -3  0 -7 -6 -5 16  3 -5
Y  -4 -4 -4 -6 -5 -3 -5 -6  3 -3 -2 -4 -3  4 -6 -3 -3  3 11 -3
V  -1 -4 -5 -6 -2 -4 -4 -6 -5  4  1 -4  1 -2 -4 -3  0 -5 -3  7
```

:::{exercise} Assignment 4
:label: blast-p1-a4
:nonumber:
What is the alignment score of the protein sequences of A and B (from Assignment 2), using the
BLOSUM80 matrix? Leave the gap out for now.
:::

:::{solution} blast-p1-a4
:class: dropdown
Score each aligned pair and add them up:

| A | W | S | S | I | L | T | A |
|---|---|---|---|---|---|---|---|
| B | W | C | S | - | L | T | A |
| Score | 16 | −2 | 7 | (gap) | 6 | 8 | 7 |

16 − 2 + 7 + 6 + 8 + 7 = **42**
:::

## Assignment 5: Gap penalties

Use the following scoring scheme for gaps: **opening a gap costs −1; each extension of a gap
costs −0.5**.

:::{exercise} Question 1
:label: blast-p1-a5-q1
:nonumber:
What is the gap penalty for the alignment of sequences A and B? What is the final score of this
alignment?
:::

:::{solution} blast-p1-a5-q1
:class: dropdown
The gap is one amino acid long, so it is only opened, not extended.

- Gap cost: −1
- Final score: 42 − 1 = **41**
:::

:::{exercise} Question 2
:label: blast-p1-a5-q2
:nonumber:
We now compare a third sequence, C, with sequence A:

```text
Sequence C: AGCAGATCGTAGGACTGACGT
```

Transcribe and translate sequence C as in Assignment 2. What is the alignment score of A and C
with the BLOSUM80 matrix?

| DNA | A | G | C | A | G | A | T | C | G | T | A | G | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
| AA  |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
:::

:::{solution} blast-p1-a5-q2
:class: dropdown
| DNA | A | G | C | A | G | A | T | C | G | T | A | G | G | A | C | T | G | A | C | G | T |
|-----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RNA | U | C | G | U | C | U | A | G | C | A | U | C | C | U | G | A | C | U | G | C | A |
| AA  | **S** | | | **S** | | | **S** | | | **I** | | | **L** | | | **T** | | | **A** | | |

| A | W | S | S | I | L | T | A |
|---|---|---|---|---|---|---|---|
| C | S | S | S | I | L | T | A |
| Score | −6 | 7 | 7 | 7 | 6 | 8 | 7 |

−6 + 7 + 7 + 7 + 6 + 8 + 7 = **36**

In fact, a better score of 40 is possible: put a one-position gap at the start of each sequence
so that W is not paired with S. That gives 42 for the aligned pairs, minus 1 for each of the two
gaps.
:::

:::{exercise} Question 3
:label: blast-p1-a5-q3
:nonumber:
What is the gap penalty for the alignment of sequences A and C? What is the final score of this
alignment?
:::

:::{solution} blast-p1-a5-q3
:class: dropdown
- Gap cost: 0, as there is no gap.
- Final score: **36**
:::

:::{exercise} Question 4
:label: blast-p1-a5-q4
:nonumber:
Describe the difference between the two alignment scores. Did you expect this outcome? Why does
codon 1 have a stronger effect on the score than codon 2 in the alignment of A and B?
:::

:::{solution} blast-p1-a5-q4
:class: dropdown
Without a gap, you might expect the alignment of 7 amino acids with 1 mismatch (A vs C) to score
higher than the alignment of 6 amino acids with 1 mismatch and 1 gap (A vs B). It does not,
because the scoring matrix takes into account how (dis)similar the paired amino acids are: their
chemical group, size and other properties.

The serine (S) in sequence C is much more different from the tryptophan (W) in sequence A
(score −6) than the cysteine (C) in sequence B is from the serine (S) in sequence A (score −2).
:::
