(blast-bg-nucleotides)=
# Alignment scoring example (for nucleotides)

:::{note}
This chapter comes from *Protein and DNA sequence alignment: finding and comparing sequences* by Susan Coort, Chris Evelo, Lars Eijssen, Egon Willighagen and Friederike Ehrhart, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), originally published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER) (version of 2023-10-16). It has been converted to the format of this book; the text is unchanged. See [Background](index.md) for details.
:::

In Case 10, the various sequences were nicely aligned: the first nucleotides of both
sequences were at the same alignment position. However, one aspect of making a new
alignment and searching for a match in a database, is that one does not know at the start
which two nucleotides form that first match.

For example, given the next two DNA sequences:

```
GCATT
   |
CAGTG
```

At first sight, does it not a good overlap. However, if we shift the alignment by one
nucleotide, it matches better:

```
GCATT
 || |
 CAGTG
```

Creating phylogenetic trees, or comparing two alignments (not sequences) in an automatic
manner, one needs a mathematical (numerical) distance. A simple approach would be as
follows: one point for each identical nucleotides, and zero points otherwise. Then, the above
two alignments have 1 (T matching T) and 3 points (CC, AA, and TT matches), respectively.

Now, say we have another, third sequence, `GCTT`. We could then make the following alignment:

```
GCATT
|| |
GCTT
```

Again, a score of three points.

## Gaps

However, we could also introduce a gap. That is, at some
point an addition or deletion happened, and evolutionary these sequences could be related
via this alignment:

```
GCATT
|| ||
GC-TT
```

But artibrarily including gaps makes it match nicely, but it should affect the total score. After
all, we can match any sequence if we can introduce gaps without penalties. This is the
background of the gap penalty. Elongation of a gap (making it longer) typically has a lower
penalty than starting a new gap. If the penalty is -1 point, then the last alignment has three
points. However, if the penalty is -2 points, then the alignment has 4-2=2 points.

Here is an example with two possible alignments, without and with gap:

```
ACTAGATCGTACGACTGACGT
|||| |||  || |  |
ACTACATCGGACTGACGT
```

```
ACTAGATCGTACGACTGACGT
|||| ||||   |||||||||
ACTACATCG---GACTGACGT
```

Which one has the higher alignment score? Also, what does the gap mean at protein level?

## Scoring Matrices

When comparing two sequences, there is a very large number of possibilities to align the two,
especially taking into account the possibility for inclusion of insertions and deletions.
In order to decide which of those possible alignments is the best one, we need a scoring scheme.
Such a scoring scheme should give an individual score for each paired residue (nucleotide, or
gap) which then can be summed over the entire alignment to get a total score that reflects
the degree of similarity. The alignment with the highest total score is then considered the
best. A very simple option would be to count the percentage identity (number of matching
residues divided by the total alignment length), but this fails to use much of the information
we have on the biological properties of sequences.

Scoring schemes for nucleotides sequences are generally quite simple (a positive score for a match,
a negative score (penalty) for a mismatch, and penalties for any included gaps). We showed examples
of this earlier on this page.
