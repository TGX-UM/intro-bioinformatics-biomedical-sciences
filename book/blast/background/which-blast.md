(blast-bg-which)=
# Which BLAST to use

:::{note}
This chapter comes from *Protein and DNA sequence alignment: finding and comparing sequences* by Susan Coort, Chris Evelo, Lars Eijssen, Egon Willighagen and Friederike Ehrhart, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), originally published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER) (version of 2023-10-16). It has been converted to the format of this book; the text is unchanged. See [Background](index.md) for details.
:::

Blast can also be used to align two sequences, but is most commonly used to compare a
sequence against all entries in a database of sequences.

The NCBI BLAST website has a few variants that people can use:

* [Nucleotide BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome) (blastn): search for similar nucleotide sequences in a nucleotide sequence database
* [blastx](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastx&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome): search protein databases using a translated nucleotide query
* [tblastn](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=tblastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome): search translated nucleotide databases using a protein query
* [Protein BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome) (blastp): search for similar protein sequences in a protein sequence database

Or, how NCBI visualizes it themselves:

```{figure} figures/blast-types.png
:alt: The BLAST programs on the NCBI BLAST home page. Screenshot of NCBI BLAST (NCBI, public domain).

The BLAST programs on the NCBI BLAST home page. Screenshot of NCBI BLAST (NCBI, public domain).
```
