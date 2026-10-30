(db-guide-why-databases)=
# Why use databases at all?

A textbook gives you a well-organised overview of a process, and for learning the basics it is hard to beat. But a textbook is written once and revised every few years, while new findings on genes, proteins and diseases appear every day. Databases are where that knowledge is collected, structured and kept up to date. They are also where you find information that no textbook would print: every known variant in a gene, its frequency in different populations, every tissue in which it is expressed, every experiment that showed two proteins interact.

## Primary and aggregating resources

It helps to know what kind of database you are looking at.

A **primary** (or core) resource is the main home of one kind of data. Its curators collect, check and publish that data, and other databases take it from them. Examples from the practicals: UniProt for protein sequences and their function, ClinVar for clinical interpretations of variants, dbSNP for the catalogue of short variants, WikiPathways for its pathway diagrams, ChEBI for curated small molecules.

An **aggregating** (or integrating) resource gathers data from many primary sources and shows it together on one page. NCBI Gene is a good example: its gene page shows expression data, phenotypes from OMIM and ClinVar, pathways via PubChem, and much more, none of which NCBI Gene produced itself. PubChem does the same for chemicals, with data from hundreds of depositors. Ensembl is partly both: it produces its own gene annotation, but imports variants from dbSNP and frequencies from population projects.

Why does this matter? Three reasons.

- **Lag.** An aggregator shows a copy of the primary data, and that copy can be months old. In October 2026, dbSNP pages still showed clinical classifications from 2024, while ClinVar itself had moved on. If the exact answer matters, go to the primary source.
- **Loss in transit.** When data is copied, detail can be dropped or simplified. A "most severe consequence" label in a summary bar, for example, is a compression of several separate facts (see the section on Ensembl).
- **Disappearance.** When a website is rebuilt, the aggregated parts are the first to go. Ensembl's new site no longer shows clinical significance or phenotypes for variants. That information still exists, in ClinVar, where it always originated.

Knowing which resource is the primary home for which kind of data is more durable knowledge than knowing the menus of one website.

## Identifiers: why stable IDs beat names

Genes and proteins have names, but names are a poor way to identify them. One gene usually has several names: IGF1 is also known as IGF-I, IGFI, somatomedin C and mechano growth factor. Different databases list different synonyms, and spell them differently (IGF-I versus IGFI). Worse, some synonyms are shared between unrelated genes, some are disease names (LFS1 for TP53, after Li-Fraumeni syndrome; HGPS for LMNA, after Hutchinson-Gilford progeria syndrome), and gene names change when the naming committee decides they should. MSTN is called "myostatin" by NCBI, but UniProt's main name for its protein is "Growth/differentiation factor 8".

Every database therefore gives each record a unique **identifier**: a code that refers to exactly one thing and does not change. The human IGF1 gene is 3479 in NCBI Gene, ENSG00000017427 in Ensembl, HGNC:5464 at the HUGO Gene Nomenclature Committee, and 147440 in OMIM. Its protein is P05019 in UniProt. When you write down or communicate which gene or protein you mean, give an identifier, not just a name. And when you search one database using a name you found in another, check that you landed on the right record, for the right species.

Databases help you here by linking to each other's identifiers (*cross-references*). Following those links is usually the safest way to get from one database to the next.

Many identifiers carry a **version number** after a dot: ENSG00000017427.19, NM_000618.5, NP_000609.1. The part before the dot stays the same for the life of the record; the number after it goes up whenever the record's sequence or structure changes. Leave the version off when you just want "the gene"; include it when you quote a number that depends on the exact record, such as a transcript count or a sequence position.

## Versions and releases: quote what you saw, and when

Because databases change, any number you take from one is a statement about *that database at that moment*, not a timeless fact about biology. A real example from this course:

On 31 August 2026, Ensembl listed 7 transcripts for the human IGF1 gene. On 22 October 2026 it listed 15. Nothing happened to the gene; Ensembl added new transcript models to its annotation. And throughout that period, the website showed the same release label, "Release 2026-07". The release label alone would not have told you that the data had changed. The gene version did: on 22 October the gene was ENSG00000017427.19.

So whenever you report a value from a database, write down three things:

1. the **database** (and, if relevant, which part of it: "NCBI Gene, RefSeq section");
2. the **version**: a release number (UniProt release 2026_03, dbSNP build 157), or, for Ensembl, the versioned identifier of the record (ENSG00000017427.19);
3. the **date** you looked.

For example: "IGF1 has 15 transcripts (Ensembl, gene ENSG00000017427.19, accessed 22 October 2026)". This is what makes a result reproducible by someone who reads your report a year later and finds a different number. It is also why scientific papers cite database versions.

## MANE Select: the one transcript everyone agrees on

Most human genes produce several transcripts (splice variants), and different databases have long made their own choice of which one is the "main" one. That was a real problem in clinical genetics: the same variant could be described at different positions depending on which transcript a laboratory used.

**MANE** (Matched Annotation from NCBI and EMBL-EBI) is a joint project of the two big annotation groups to fix this. For each protein-coding human gene they agree on one representative transcript, the **MANE Select** transcript, and make sure that it is identical, base for base, in both databases. In Ensembl it has an ENST identifier, in NCBI an NM_ identifier, and the two are labelled as each other's match. For IGF1 the MANE Select transcript is ENST00000337514.11 in Ensembl and NM_000618.5 in RefSeq.

A few points to remember:

- MANE Select is chosen because it is well supported and biologically representative, **not because it is the longest**. The MANE Select transcript of IGF1 encodes 153 amino acids; other IGF1 transcripts encode 195.
- MANE Select is the default transcript for reporting variants. When dbSNP, ClinVar or Ensembl give a consequence "on the MANE Select transcript", they all mean the same sequence.
- A few genes have a second MANE transcript, labelled **MANE Plus Clinical**, where one transcript is not enough to report all clinically relevant variants. LMNA is an example: lamin A (NM_170707.4) is MANE Select, lamin C (NM_005572.4) is MANE Plus Clinical.
- UniProt's *canonical* protein sequence is chosen by UniProt's own rules and need not be the MANE protein. For IGF1, UniProt's canonical sequence is the 195-residue form. Expect different databases to report different "lengths" for the same protein.

More information: <https://www.ncbi.nlm.nih.gov/refseq/MANE/> and <https://www.ensembl.org/info/genome/genebuild/mane.html>.
