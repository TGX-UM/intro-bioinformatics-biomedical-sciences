(blast-bg-comparing)=
# Comparing Sequences

:::{note}
This chapter comes from *Protein and DNA sequence alignment: finding and comparing sequences* by Susan Coort, Chris Evelo, Lars Eijssen, Egon Willighagen and Friederike Ehrhart, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), originally published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER) (version of 2023-10-16). It has been converted to the format of this book; the text is unchanged. See [Background](index.md) for details.
:::

There are several applications in biomedical science that need to compare DNA, RNA or protein sequences:
* trying find a matching sequence in a database for a sequence you found in an experiment or
* comparing two sequences to determine the similarity and possible evolutionary relationship.
This comparison is done by the basic local alignment search tool (BLAST). 

The first step of BLAST in any of these comparisons is to find the best alignment.

This sequence alignment is done by (pairwise) sequence alignment, defined as the process of
arranging two sequences to achieve maximal levels of identity and conservation.

* Identity: A residue is exactly the same (either nucleotide or amino acid)
* Conservation: An amino acid is replaced by another amino acid that preserves the
  physicochemical properties of the original residue (for nucleotides, conservation
  has no meaning, as due to the triplet code translation, two DNA/RNA residues can only be identical or not for the meaning of the code)
* Similarity: The resulting extent to which sequences are related, based on identity and conservation.

For conservation, the group to which an amino acid belongs is important (basic, acidic,
uncharged polar, or nonpolar side chain), as well as the size of the amino acid’s side chain.
Also, some amino acids have very unique properties, making them essential in certain positions
in a protein (e.g. cysteine, to form sulphur bridges).

Homology is defined as similarity attributed to descent from a common ancestor. Sequences
are either homologous or not (they cannot be somewhat homologous due to similar protein domain function). Orthologues are homologues
between species (e.g. human and mouse haemoglobin alpha chain), paralogues are homologues
within a species (e.g. human haemoglobin alpha and beta chain).

Using sequence alignment allows us to assess the degree of similarity and the possibility of homology.

Besides checking identity and conservation of residues, we also should be able to account for
the occurrence of (small) insertions and deletions. This is done by the concept of a gap:
when aligning two sequences, each of them can be broken apart, and some residues in the other
sequence can be matched to empty spaces in that sequence.

## Comparing protein or nucleotide sequences?

Alignment of protein sequences can be more informative than alignment of nucleotide
sequences. This has several reasons:

* There are 20 different amino acids, but only 4 different nucleotide bases
* For amino acids we can take their biophysical similarities into account
* Codons are degenerate: changes in the third position of coding sequences often do not alter
  the amino acid that is specified

So, protein sequences offer a longer “look-back” time.

This means that it can be more useful to use protein sequences than DNA or RNA sequences,
especially when the expected divergence between the sequences is high (e.g. large evolutionary
distance).

Alignment of nucleotide sequences is still useful, for example to:

* study noncoding regions of DNA (promoter regions, intergenic regions)
* confirm the identity of a cDNA
* study DNA polymorphisms
* study genomes (compare genomes, create genome annotations)
