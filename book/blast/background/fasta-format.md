(blast-bg-fasta)=
# The FASTA format

:::{note}
This chapter comes from *Protein and DNA sequence alignment: finding and comparing sequences* by Susan Coort, Chris Evelo, Lars Eijssen, Egon Willighagen and Friederike Ehrhart, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), originally published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER) (version of 2023-10-16). It has been converted to the format of this book; the text is unchanged. See [Background](index.md) for details.
:::

The FASTA format is a text-based format for nucleotide sequences or protein sequences.
It represents the nucleotides or amino acids of the sequences using single-letter codes.
A simple example looks like this:

```text
>P01013 GENE X PROTEIN (FIRST PART)
QIKDLLVSSSTDLDTTLVLVNAIYFKGMWKTAFNAEDTREMPFHVTKQESKPVQMMCMNNSFNVATLPAE
KMKILELPFASGDLSMLVLLPD
```

The format starts with a comment line, commonly started with a `>` and giving information about the protein (here a Uniprot ID) and other experimental relevant information. The following lines contain the actual sequence.

The pattern can be repeated to create a multiple sequence FASTA file, where each time
a comment line indicates the start of the next sequence.

## More info

* [NCBI BLAST Help page](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=BlastHelp)
* [Wikipedia: FASTA format](https://en.wikipedia.org/wiki/FASTA_format)
