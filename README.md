# Introduction to Bioinformatics for Biomedical Sciences

An open, CC BY 4.0 e-book that brings together the bioinformatics computer practicals of the
Biomedical Sciences bachelor at Maastricht University. Every practical runs in a web browser; no
installation or programming is needed.

Read it online: https://tgx-um.github.io/intro-bioinformatics-biomedical-sciences/

| Module | Course | Status |
|---|---|---|
| 1. Sequence alignment and BLAST | BBS1001 | Available |
| 2. Biological databases | BBS2002 | In preparation |
| 3. Cell signalling | BBS2042 | Planned |

## Building the book

The book is built with [TeachBooks](https://teachbooks.io) (Jupyter Book v1), the same setup
Maastricht University Press uses for its open textbooks. Every push to `main` is built and
published to GitHub Pages by `.github/workflows/call-deploy-book.yml`.

To build locally:

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
teachbooks build book          # output in book/_build/html/index.html
```

## Adding a module

1. Create a folder under `book/` named after the module, with an `index.md` (course, time, what
   you will learn, background reading) and one page per assignment or case.
2. Put each question in an `exercise` block and its answer in a `solution` block with
   `:class: dropdown` (see `book/blast/` for examples). Note at the top of each page the date the
   answers were checked against the live resources.
3. Add the module as a new part in `book/_toc.yml` and to the module table in `book/intro.md`.
4. List every third-party figure or screenshot, with its licence, in `THIRD-PARTY.md`.

## Licence

Text and exercises: [CC BY 4.0](LICENSE). Third-party content keeps its own terms; see
[THIRD-PARTY.md](THIRD-PARTY.md).

Developed with an OpenUP grant from Maastricht University (2026–2027).
