(blast-background)=
# Background: sequence alignment and BLAST

*Reading time: about 30 minutes.*

These chapters explain the ideas behind the exercises: why we compare DNA, RNA and protein
sequences, how an alignment is scored, how PAM and BLOSUM matrices are made, which BLAST program
to use, and how to read BLAST output. Read them before the workshop, or come back to them when a
question in the exercises sends you here.

1. [Introduction](introduction.md)
2. [Comparing sequences](comparing-sequences.md)
3. [Alignment scoring example (for nucleotides)](scoring-nucleotides.md)
4. [Alignment scoring example (for proteins)](scoring-proteins.md)
5. [Which BLAST to use](which-blast.md)
6. [Interpreting BLAST output](blast-output.md)
7. [The FASTA format](fasta-format.md)

## How the chapters match the exercises

Each chapter ends with a box that lists the exercises using it. The same links appear the other
way round at the top of each exercise page.

| Chapter | Part 1 | Case 1 | Case 2 | Case 3 | Case 4 |
|---|:-:|:-:|:-:|:-:|:-:|
| [Introduction](introduction.md) | ✓ | ✓ | | ✓ | |
| [Comparing sequences](comparing-sequences.md) | ✓ | ✓ | ✓ | | ✓ |
| [Alignment scoring example (for nucleotides)](scoring-nucleotides.md) | ✓ | | | | |
| [Alignment scoring example (for proteins)](scoring-proteins.md) | ✓ | ✓ | | | |
| [Which BLAST to use](which-blast.md) | | ✓ | ✓ | ✓ | ✓ |
| [Interpreting BLAST output](blast-output.md) | | ✓ | ✓ | ✓ | ✓ |
| [The FASTA format](fasta-format.md) | | ✓ | | | |

The questions inside the Introduction are part of the original resource and have no worked
solution in this book.

## Origin and credits

This section is the Open Educational Resource *Protein and DNA sequence alignment: finding and
comparing sequences*, an introduction to sequence alignment and BLAST for first-year Biomedical
Sciences students, written at Maastricht University between 2020 and 2023 by:

- Susan Coort ([ORCID](https://orcid.org/0000-0003-1224-9690))
- Chris Evelo ([ORCID](https://orcid.org/0000-0002-5301-3142))
- Egon Willighagen ([ORCID](https://orcid.org/0000-0001-7542-0286))
- Lars Eijssen ([ORCID](https://orcid.org/0000-0002-6473-2839))
- Friederike Ehrhart ([ORCID](https://orcid.org/0000-0002-7770-620X))

It was first published at [github.com/BiGCAT-UM/BLAST-OER](https://github.com/BiGCAT-UM/BLAST-OER)
under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) licence. The chapters here
follow the version of 16 October 2023 (commit `8a911e2`).

Changes made when bringing it into this book: the chapters were converted to the book's format
(navigation links replaced by the book's own, images turned into numbered figures with credits,
links between chapters updated), and each chapter got a closing box, written for this book, that
links it to the exercises. Since then, typos, a wrong score example, an outdated
course reference and two broken links have been corrected; see the [changelog](../../changelog.md).
One figure, a Proteopedia
rendering of the β-hemoglobin glutamate, was left out because its licence (GNU FDL) is not
compatible with this book; the text still links to the
[Proteopedia page](https://proteopedia.org/wiki/index.php/Hemoglobin). Further corrections
are tracked as [issues](https://github.com/TGX-UM/intro-bioinformatics-biomedical-sciences/issues).

(blast-bg-material)=
## Educational material

Videos by the National Center for Biotechnology Information (NCBI):

- [NCBI Minute: A Beginner's Guide to Genes and Sequences at NCBI](https://www.youtube.com/watch?v=QIZ8QH6JcC8) (33:43 min)
- [Webinar: A Practical Guide to NCBI BLAST](https://www.youtube.com/watch?v=KLBE0AuH-Sk) (54:44)
- [BLAST Results: Expect Values, Part 1](https://www.youtube.com/watch?v=ZN3RrXAe0uM) (2:29)
- [BLAST Results: Expect Values, Part 2](https://www.youtube.com/watch?v=dzRq-5BrGD4) (3:39)
- [NCBI Minute: Five Teaching Examples Using BLAST](https://www.youtube.com/watch?v=JKD5laNtwSc) (29:37) ([booklet](https://ftp.ncbi.nlm.nih.gov/pub/factsheets/Booklet_Teaching_BLAST.pdf))
- [NCBI Minute: Using BLAST Well](https://www.youtube.com/watch?v=2FW1dk5YQ3I) (45:53)

More training material on BLAST can be found in the
[ELIXIR Training Portal TeSS](https://tess.elixir-europe.org/search?q=blast).

## Literature

- {cite:t}`mount2007`
- {cite:t}`henikoff1992`
- {cite:t}`altschul1990`
