(db-guide-wikipathways)=
# WikiPathways

**What it is.** WikiPathways, <https://www.wikipathways.org/>, is an open, community-curated database of biological pathway diagrams, maintained by teams at Maastricht University (Department of Translational Genomics) and the Gladstone Institutes in San Francisco. Anyone can contribute or correct a pathway; curators review the changes. All content is CC0, free for any reuse.

**What question it answers.** In which processes does this gene or compound take part? What acts upstream and downstream of it? Is it stimulated or inhibited, and by what?

**Getting there.** Search by pathway name, gene or compound on the home page, or go directly to a pathway by its identifier: <https://www.wikipathways.org/pathways/WP3932.html>. Pathways exist per species; make sure you open the *Homo sapiens* version.

## The pathway page

The top of the page shows the pathway's title, identifier, species and a **last edited** badge with the date of the most recent change. Below that is the diagram, then a description of the pathway, its authors, and a **Share this pathway** box with a ready-made citation that includes the last-edited date. Further down are ontology terms (Pathway Ontology, disease and cell-type terms), the **Participants** table, the **References** and **Download** options (GPML, PNG, SVG and others).

The **Participants** table lists every element in the diagram with its **Label** (the text in the box), its **Type** (GeneProduct, Protein, Metabolite, and so on), its **Compact URI** (the database identifier, written as `database:identifier`, such as `ensembl:ENSG00000140443` or `chebi:29120`) and any **Comment** left by curators. Clicking the identifier takes you, via bioregistry.io, to that record in the source database. The Participants table is the most reliable way to get from a box in the diagram to a gene, protein or compound record, and it is also searchable with your browser's find-in-page.

## The interactive viewer

Click the diagram to open the interactive pathway viewer in a new tab. There you can zoom and pan, and click any box to see its identifiers and follow the link to the source database.

The viewer can also highlight elements for you, which helps on large diagrams. Add colour names and labels to the address:

<https://pathway-viewer.toolforge.org/embed/WP3932?lightgreen=IGF1&red=IGF1R>

This opens WP3932 with IGF1 highlighted in light green and IGF1R in red. Your browser's find-in-page does not work well on a wide diagram: it finds the label but cannot scroll the drawing to it. If the viewer is unavailable (it runs on a separate server and is occasionally down), use the Participants table instead.

## Reading the diagram

Pathway diagrams follow a graphical convention, explained in the *WikiPathways Legend* linked below the description on the pathway page:

- **Boxes** are entities. Black-bordered boxes are genes or gene products (proteins); blue boxes are metabolites and other small molecules. Groups of boxes drawn together form a complex or a family.
- **Lines** are interactions. An ordinary **arrow** usually means a positive effect: stimulation, activation, or a conversion from one molecule into another. A line ending in a **T-bar** (a short perpendicular line) means **inhibition**. Other end shapes mark catalysis (an enzyme acting on a conversion), binding, or transcriptional regulation. Read the arrowheads carefully: "A inhibits B, which inhibits C" means A indirectly *activates* C.
- **Labels** without a border (text only) give context, such as a cell compartment, a process name or a group heading, like "Growth factors" or "RTK".
- **Cell compartments**: membranes are often drawn as lines or shapes. In WP3932, the double vertical line is the plasma membrane, with the extracellular molecules on the left.

## Pitfalls

- **Diagrams are curated by people, and people make mistakes.** In WP3932, the box labelled "NO" (nitric oxide) is annotated with CHEBI:29120, which is the nitrosonium cation NO⁺, not the nitric-oxide radical (CHEBI:16480) that acts as a signalling molecule. Check that an identifier describes what the label says. Being a wiki, WikiPathways lets you report or fix such errors.
- **A label is not an identifier.** The diagram may say "IGF-1" in one place and "IGF1" in another, and only one may carry a gene identifier. Use the box that links out, or the Participants table.
- **Not every pathway uses the same database for compounds.** Most use ChEBI, but some use HMDB (Human Metabolome Database) or others. You may need to translate.
- **Some human pathways were converted from mouse or rat**, which shows in the Comment column ("Homology Mapping from Mus musculus to Homo sapiens"). The interactions were described in the other species.
- **The last-edited date moves with every edit.** Quote the date you saw.
