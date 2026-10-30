(db-guide-pubchem)=
# PubChem

**What it is.** PubChem, <https://pubchem.ncbi.nlm.nih.gov/>, is NCBI's open chemistry database and one of the largest chemical collections in the world. It **aggregates** information from hundreds of depositors: chemical suppliers, other databases, journals, government agencies and screening centres.

PubChem has three linked collections: **Substances** (SID; each record as deposited by a source), **Compounds** (CID; one per unique chemical structure, merging substances with the same structure) and **BioAssays** (AID; results of biological screening experiments). For most purposes you want the **compound**, identified by its **CID**.

**What question it answers.** Everything that has been reported about a compound: names and identifiers, physical and chemical properties, drug and medication information, pharmacology, safety and hazards (GHS classification), toxicity, bioassay results, patents, suppliers, literature, and the pathways and genes it interacts with.

**Getting there.** Type a name, formula or identifier in the search box. Or go directly by CID: <https://pubchem.ncbi.nlm.nih.gov/compound/5757> (estradiol).

## A compound page

A compound page is long and divided into sections, with a table of contents: Structures, Names and Identifiers, Chemical and Physical Properties, Related Records, Drug and Medication Information, Pharmacology and Biochemistry, Safety and Hazards, Toxicity, Literature, Patents, Interactions and Pathways, Biological Test Results, Taxonomy and Classification, among others. Each piece of information shows its source. Not every compound has every section.

## Pitfalls

- **Several hits for one name.** A search for "insulin" returns human insulin, insulins from other species and modified forms, because each distinct structure is its own compound. Pick by name and formula.
- **One name, different charge state.** A search for "nitric oxide" finds CID 145068, the neutral molecule. It is not the same entity as the NO⁺ cation in ChEBI's CHEBI:29120.
- **Aggregated means mixed quality and mixed terms.** Each section comes from a named depositor with its own reliability and its own terms of use. Check the source.
- **PubChem and ChEBI complement each other.** Use ChEBI for a precise, curated identity and roles; use PubChem for the breadth of what has been reported.
