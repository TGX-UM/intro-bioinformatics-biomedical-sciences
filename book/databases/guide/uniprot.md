(db-guide-uniprot)=
# UniProt

**What it is.** UniProt, <https://www.uniprot.org/>, is the central database of protein sequences and their function, run by a consortium of EMBL-EBI, the SIB Swiss Institute of Bioinformatics and the Protein Information Resource (PIR) in the USA. Its main part, **UniProtKB**, has two sections:

- **Reviewed (Swiss-Prot)**: entries curated by experts, who read the literature and summarise it with references and evidence. About 576,000 entries, about 20,400 of them human (release 2026_03).
- **Unreviewed (TrEMBL)**: entries annotated automatically, mostly from translated genome sequences. Close to 150 million entries.

For a well-studied human protein there is nearly always one reviewed entry, and that is the one to use. Restrict your search to "Reviewed" and to *Homo sapiens*.

**What question it answers.** What does this protein do, where in the cell is it, which diseases and variants are linked to it, how is it processed and modified, what does it interact with, which isoforms exist, and what is known about its structure? With references and evidence for each statement.

**Getting there.** Search by gene symbol or protein name, then filter to reviewed human entries. Or open an entry directly by accession: <https://www.uniprot.org/uniprotkb/P05019/entry>. NCBI Gene and Ensembl link to it.

## The entry page

Tabs at the top switch between the **Entry** itself, the **Variant viewer**, the **Feature viewer**, **Publications**, **External links** and **History**. The Entry tab is divided into sections, listed in a menu on the left:

- **Function**: a written description of what the protein does, with numbered references; subsections such as Miscellaneous, Catalytic activity and Pathway where relevant; and the **GO annotations** (see below).
- **Names & Taxonomy**: the recommended name, alternative names, gene name and organism. The recommended name can differ from the gene name: the MSTN protein is "Growth/differentiation factor 8", LMNA's is "Prelamin-A/C".
- **Subcellular Location**: where the protein is found in the cell, as annotated by UniProt curators and, in a second tab, by GO cellular-component annotation, shown on a cell drawing.
- **Disease & Variants**: diseases in which the protein is involved, with a short description, the OMIM number, and a table of **natural variants** linked to that disease, with their positions, changes and dbSNP rs numbers where known. Also mutagenesis experiments.
- **PTM/Processing**: how the protein is processed and modified after translation: the signal peptide, propeptides and mature chain(s) with their positions, and modified residues such as phosphoserine.
- **Expression**: tissue specificity and developmental stage, when curators have written it. Many entries have none.
- **Interaction**: the subunit structure and a table and figure of **binary interactions** (from the IntAct database), with the number of experiments that support each interaction.
- **Structure**: experimentally determined 3D structures (from the PDB) and the predicted AlphaFold model.
- **Family & Domains**: domains, repeats, regions and motifs along the sequence.
- **Sequence & Isoforms**: the canonical sequence and its length, and any other isoforms.

## GO annotations and evidence codes

The **Gene Ontology** (GO) is a controlled vocabulary for describing what gene products do, in three aspects: **molecular function** (for example *protein kinase activity*), **biological process** (for example *DNA damage response*) and **cellular component** (for example *nucleus*). Each term has an identifier, such as GO:0006974.

In the Function section, UniProt shows the GO terms for the protein as a ribbon of categories, with a table below. Click a category, such as "All Biological Process", to filter the table. Each annotation has an **evidence code**, which tells you how it was made:

| Code | Meaning | Strength |
|---|---|---|
| IDA | Inferred from Direct Assay: an experiment showed it directly for this protein | strong, experimental |
| IMP | Inferred from Mutant Phenotype: shown by mutating or knocking out the gene | strong, experimental |
| IPI | Inferred from Physical Interaction | experimental |
| IBA, ISS | inferred from evolutionary relationships or sequence similarity to other proteins | inferred |
| IEA | Inferred from Electronic Annotation: assigned automatically, not checked by a curator | weakest |
| TAS, NAS | statements by authors, traceable or not to a source | author statements |

When you need to rely on a function, prefer annotations with experimental evidence and look at the reference given. See <https://geneontology.org/docs/guide-go-evidence-codes/>.

## Isoforms

UniProt describes protein **isoforms**, not transcripts. Several transcripts that encode the same protein count as one isoform. Each isoform has an identifier made of the accession plus a number: P05019-1, P05019-2, and so on. One isoform is the **canonical** sequence, the one shown by default and used for position numbering in the entry; UniProt chooses it by its own criteria (often the most common or longest form), so it need not match the MANE Select protein. See <https://www.uniprot.org/help/canonical_and_isoforms>.

Polymorphisms are not isoforms. The APOE E2, E3 and E4 forms are the same protein from different alleles, so UniProt lists one APOE isoform.

## The Feature viewer

The **Feature viewer** tab draws all annotated features (domains, regions, PTMs, variants, structures) as tracks along the sequence, so you can see where they lie relative to each other. In 2025 UniProt removed the "Structural features" group that used to show helices, strands and turns. No track shows them now: the **PDBe 3D structure coverage** and **AlphaFold** tracks show which parts of the protein are structured, and the 3D viewer in the *Structure* section of the entry page shows those parts, with helices drawn as spirals and strands as arrows.

## Pitfalls

- **Check that you are in a reviewed, human entry.** Unreviewed entries exist for the same protein from many sources, with less reliable annotation.
- **Positions in UniProt refer to the canonical isoform**, including the signal peptide. Compare with the PTM/Processing section to translate to mature-protein numbering.
- **Natural variants tables are selective**, like OMIM's allelic variants. The Variant viewer tab lists many more, from large-scale sources.
- **Interaction colour means support, not strength.** Darker dots in the binary-interaction figure have more experiments behind them; they say nothing about binding affinity.
- **Not every entry has every section filled.** "No tissue specificity text" is common and means only that curators did not write one.
