(db-guide-chebi)=
# ChEBI

**What it is.** ChEBI, *Chemical Entities of Biological Interest*, <https://www.ebi.ac.uk/chebi/>, is a curated dictionary of small molecules at EMBL-EBI. It describes what a chemical entity *is* (structure, formula, charge, names) and how it relates to other entities and to biological **roles**, using an ontology. The website was rebuilt as **ChEBI 2.0** in October 2025; identifiers stayed the same. Its content is CC BY 4.0.

**What question it answers.** What exactly is this compound, and how does it relate to similar ones? What biological roles does it have (hormone, metabolite, vasodilator, drug)? Which identifier should I use for it?

**Getting there.** Search by name, formula or identifier on the home page, or go directly to `https://www.ebi.ac.uk/chebi/CHEBI:16469`. WikiPathways boxes for metabolites usually link to ChEBI.

## An entry

A ChEBI entry gives the ChEBI name, identifier and a star rating (three stars means manually annotated by ChEBI curators), a **definition**, the structure drawing, formula, charge and mass, synonyms and IUPAC name, cross-references to other databases, and the **ontology**: the relationships of this entity to others. The relationships you will meet most:

- **is a**: classification. 17β-estradiol *is a* estradiol, which is a steroid.
- **has role**: a biological, chemical or application role. Nitric oxide *has role* signalling molecule, vasodilator agent, neurotransmitter, human metabolite.
- **is conjugate acid of / is conjugate base of**: the same molecule in different protonation states. (S)-lactate (CHEBI:16651, charge −1) *is conjugate base of* (S)-lactic acid (CHEBI:422). In the body, at pH 7.4, the charged form usually dominates.
- **is enantiomer of**, **is tautomer of**, **has functional parent**: other structural relationships.

## Roles versus structures

Not every ChEBI entry describes one molecule. Some describe a **class** of molecules, and some a **role** that many structures can play. CHEBI:50114 *estrogen* is a role: "a hormone that stimulates or controls the development and maintenance of female sex characteristics in mammals by binding to oestrogen receptors". It has no structure or formula of its own; estrone, estradiol, estriol and synthetic compounds all *have role* estrogen. A pathway box "Estrogens" annotated with CHEBI:50114 therefore means the whole group. For the main human estrogen, look up 17β-estradiol, CHEBI:16469.

## Charge states and radicals

ChEBI gives each charge state and each radical its own entry, because they are chemically different things. Nitric oxide shows why this matters:

| | CHEBI:16480 | CHEBI:29120 |
|---|---|---|
| ChEBI name | nitric oxide | oxidonitrogen(1+) |
| What it is | the neutral free radical NO• | the nitrosonium cation NO⁺ |
| Charge | 0 | +1 |
| Roles | signalling molecule, vasodilator agent, neurotransmitter, human metabolite, and others | none listed |

The biological signalling molecule is CHEBI:16480. A database that links "NO" to CHEBI:29120 (as WikiPathways WP3932 does) points at a different chemical.

## Pitfalls

- **Same formula, different entity.** Formula and name alone do not settle identity; check charge, structure and definition.
- **Roles are not structures.** If an entry has no structure, it is probably a role or a broad class.
- **Choose the form you mean.** For an acid, ChEBI usually has both the neutral acid and its anion; the anion is the physiological form.
