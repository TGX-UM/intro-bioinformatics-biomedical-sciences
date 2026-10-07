(blast-bg-output)=
# Interpreting BLAST output

:::{note}
This chapter comes from *Protein and DNA sequence alignment: finding and comparing sequences* by Susan Coort, Chris Evelo, Lars Eijssen, Egon Willighagen and Friederike Ehrhart, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), originally published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER) (version of 2023-10-16). It has been converted to the format of this book; the text is unchanged. See [Background](index.md) for details.
:::

The [NCBI BLAST](which-blast.md) output first reports a ‘search summary’ (click to open),
which gives a summary of the parameter settings of the BLAST run. Then, for protein BLAST,
an overview of recognised known protein domains is given, if any. Then, the hits are displayed
in a graphical overview, where each hit has a colour code depending on its score. To save
space, hits from different parts of the input sequence may be placed next to each other.
These are not connected with a line. When connected with a thin line, hits represent
multiple sub hits to the same sequence in the database.

Below the graphical overview, the hits are presented in a tabular format, indicating the name
of the hit (‘Description’), the Max score, Total score, Query Cover, E value, Ident(ity), and
Accession code. The columns have the following interpretation:

* ***Max score*** indicates the score of the best sub hit to that database entry;
* ***Total score*** indicates the summed score of all sub hits to that database entry. Note that Max and Total score are often the same, when there is only one hit to that database entry;
* ***Query coverage*** indicates which percentage of the input sequence is aligned to that database hit;
* ***Identity*** gives the percentage of residues (either nucleotides or amino acids) that are identical in the alignment between the input sequence and the database hit;
* ***Accession code*** gives the database identifier of the hit;
* ***E-value***, explained below (see also the [video's by NCBI](#blast-bg-material)).

The expect value E of a score S is the number of alignments with scores greater than or
equal to S that are expected to occur by chance in the specific database search. This is
related to the probability that the alignment occurred by chance, given the formula
p = 1 – e<sup>-E</sup>. For very small E-values, these can be interpreted as the probability
that the hit occurred by random chance (for example, for E = 0.0001, the corresponding
p = 0.0001), for high E-values it represents the number of hits to be expected by random
chance (for example, for E = 10 one expects 10 hits with at least the same score by chance).

The score and E-value are not always easy to interpret as longer less exact matches and
short exact matches will lead to similar values. It requires interpretation of the
results (and of the biology) to determine the relevance of each hit. Also, hits may only
be against known-protein domains that occur in many proteins, which are not necessarily
related or homologous to the input protein.

## Max and Total scores

Let's take the following example:

```
tggcttagta gaagttgaaa aaggcgtttt gcctcaactt gaacagccct atgtgttcat
|||||||||| ||||||||||            |||||||||| |||||||||| ||||||||||
tggcttagta gaagttgaaa ggccccaaaa gcctcaactt gaacagccct atgtgttcat
```

Here, the max score is 15, while the total score is 25.

Only if the alignment consists of one continued alignment without gaps,
then the max and total score is identical.
