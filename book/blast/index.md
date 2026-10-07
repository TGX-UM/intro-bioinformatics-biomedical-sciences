(blast)=
# Sequence alignment and BLAST

*Course: BBS1001, bachelor Biomedical Sciences, year 1. Total time: about 2 hours.*

Comparing sequences is one of the most common things a biomedical scientist does with a
computer. Is this gene the same as that one? Which organism did this DNA come from? Where does a
patient's sequence differ from the reference? This workshop answers those questions with
**BLAST** (Basic Local Alignment Search Tool) {cite}`altschul1990`, the sequence search tool run
by NCBI.

## Introductory lecture

:::{note}
A recording of the introductory lecture will be added here.
:::

<!-- Lecture recording: replace the note above with the embed, for example
:::{iframe} https://www.youtube.com/embed/<video-id>
:width: 100%
Introductory lecture: sequence alignment and BLAST.
:::
-->

## What you will learn

After this workshop you can:

- align two short DNA sequences by hand and describe their identity, mismatches and gaps
  (Part 1; background: [Comparing sequences](background/comparing-sequences.md),
  [Alignment scoring example (for nucleotides)](background/scoring-nucleotides.md));
- transcribe and translate a DNA sequence and explain how a mutation can change the protein
  (Part 1; background: [Introduction](background/introduction.md));
- choose a suitable PAM or BLOSUM substitution matrix and score a protein alignment with gap
  penalties (Part 1 and Case 1; background:
  [Alignment scoring example (for proteins)](background/scoring-proteins.md));
- choose the right BLAST program (BLASTp, BLASTx, BLASTn) and database for a question (Cases 1–4;
  background: [Which BLAST to use](background/which-blast.md));
- read a BLAST result: score, E-value, percentage identity, query coverage, and the alignments
  themselves (Cases 1–4; background: [Interpreting BLAST output](background/blast-output.md));
- use BLAST to compare paralogous proteins, find a gene in a poorly annotated genome, identify a
  bacterium from its 16S rRNA gene, and locate a disease-causing mutation (Cases 1–4).

## Before you start

You need a web browser and nothing else. The second part uses the NCBI BLAST website at
[blast.ncbi.nlm.nih.gov](https://blast.ncbi.nlm.nih.gov).

Read the [Background](background/index.md) chapters first, or keep them open while you work.
They were written for first-year Biomedical Sciences students and cover the theory behind each
part. The outline below shows which chapters go with which part, and each exercise page links to
its chapters at the top and at the questions they help with.

NCBI's own [*A Practical Guide to NCBI BLAST*](https://www.youtube.com/watch?v=KLBE0AuH-Sk) is a
good overview video.

## Workshop outline

| Part | Topic | BLAST program | Background | Time |
|---|---|---|---|---|
| [Background](background/index.md) | Sequence comparison, scoring matrices, BLAST programs and output | none | all seven chapters | 30 min reading |
| [Part 1](part1-pairwise-alignment.md) | Pairwise sequence alignment by hand: a recap of the lecture | none | [Introduction](background/introduction.md), [Comparing sequences](background/comparing-sequences.md), [Scoring (nucleotides)](background/scoring-nucleotides.md), [Scoring (proteins)](background/scoring-proteins.md) | 30 min |
| [Case 1](case1-hemoglobin.md) | Hemoglobin α and β subunits | BLASTp (two sequences) | [Introduction](background/introduction.md), [Comparing sequences](background/comparing-sequences.md), [Scoring (proteins)](background/scoring-proteins.md), [Which BLAST](background/which-blast.md), [FASTA format](background/fasta-format.md), [BLAST output](background/blast-output.md) | 30 min |
| [Case 2](case2-avian-lactase.md) | An unknown chicken transcript | BLASTx | [Comparing sequences](background/comparing-sequences.md), [Which BLAST](background/which-blast.md), [BLAST output](background/blast-output.md) | 20 min |
| [Case 3](case3-16s-pathogen.md) | A food-borne pathogen | BLASTn (16S rRNA) | [Introduction](background/introduction.md), [Which BLAST](background/which-blast.md), [BLAST output](background/blast-output.md) | 20 min |
| [Case 4](case4-rett-mecp2.md) | A gene behind Rett syndrome | BLASTn | [Comparing sequences](background/comparing-sequences.md), [Which BLAST](background/which-blast.md), [BLAST output](background/blast-output.md) | 10 min |

Read the background before the workshop. Do Part 1 first; the four cases can be done in any order.

:::{tip}
The NCBI BLAST form remembers the last database you used. If you run Case 3 (16S rRNA) before
Case 4, check that the database is set back to the default before you start Case 4.
:::
