(db-p1-a1)=
# Assignment 1: Genetic variants in the IGF1 gene in OMIM

*Time: 30 min.*

:::{note}
Answers checked against the live databases between 22 and 28 October 2026. Each answer says
when, and against which release, it was checked. Databases are updated all the time, so your
numbers may differ.
:::

*Background: the [Reference guide](../guide/index.md) has one page per database.*

“The somatomedins, or insulin-like growth factors (IGFs), comprise a family of peptides that play important roles in mammalian growth and development.” \[OMIM: 147440\].

Look up the IGF1 gene in OMIM (<https://omim.org/>), a database from Johns Hopkins University that contains expert-curated information on the links between genes and genetic variants and human disease.

:::{exercise} Question 1
:label: db-p1a1-q1
:nonumber:
To which disease has this gene been linked? Which identifier is mentioned for this disease (displayed in the table as “Phenotype MIM number”) and with which inheritance pattern?
:::

:::{solution} db-p1a1-q1
:class: dropdown
Insulin-like growth factor I deficiency (growth delay due to IGF1 deficiency), phenotype MIM number 608747, inheritance AR = autosomal recessive.

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 2
:label: db-p1a1-q2
:nonumber:
What is the alternative name of Insulin-like Growth Factor (IGF1)?
:::

:::{solution} db-p1a1-q2
:class: dropdown
SOMATOMEDIN C

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 3
:label: db-p1a1-q3
:nonumber:
How many literature references have been used to construct this page for OMIM, and when was the page last updated?
:::

:::{solution} db-p1a1-q3
:class: dropdown
Count the numbered entries under REFERENCES; the last update is the top line of *Edit History*. At the time of writing that was 82 references, last updated 10/07/2026 (OMIM writes month/day/year: 7 October 2026).

⚠️ **Release-volatile** — OMIM entries are re-curated. Report what you see.

*Checked 2026-10-24, OMIM checked by hand.*
:::

Open the Table View of Allelic Variants for the IGF1 gene: click **Table View** next to the ALLELIC VARIANTS heading (it is also linked from the left-side menu), or go straight to <https://omim.org/allelicVariants/147440>.

:::{exercise} Question 4
:label: db-p1a1-q4
:nonumber:
How many mutations are described in OMIM and which types of mutations do they include?
:::

:::{solution} db-p1a1-q4
:class: dropdown
3 variants:

- .0001: deletion of exons 4–5.
- .0002: point mutation (transversion) T\>A.
- .0003: point mutation (transition) G\>A, which changes an amino acid (valine to methionine).

*Checked 2026-10-24, OMIM checked by hand.*
:::

:::{exercise} Question 5
:label: db-p1a1-q5
:nonumber:
Which phenotype has been associated with the described variants?
:::

:::{solution} db-p1a1-q5
:class: dropdown
INSULIN-LIKE GROWTH FACTOR I DEFICIENCY

*Checked 2026-10-24, OMIM checked by hand.*
:::

Take a closer look at variant 147440.0003 — either the `.0003` row in the Table View, or the section headed `.0003 INSULIN-LIKE GROWTH FACTOR I DEFICIENCY` on the main entry page (<https://omim.org/entry/147440#0003>). Note the Table View shortens the number to `.0003`.

:::{exercise} Question 6
:label: db-p1a1-q6
:nonumber:
Answer the following questions:

a) Which change(s) in the protein are reported?

b) At which position in the protein is this change reported?

c) What is the rs number of this variant (also known as SNP)?

d) Which base is changed in the gene?

e) What is the consequence of this change?

f) How many literature references have described this variant? Describe in your own words what these references found on the influence of this particular variant on the protein.
:::

:::{solution} db-p1a1-q6
:class: dropdown
a) Valine to methionine.

b) Position 44 (V44M). OMIM numbers the *mature* IGF-1 peptide. dbSNP and ClinVar number the full precursor protein on the MANE transcript `NM_000618.5`, and there the same change is called p.Val92Met. Same variant, two numbering systems: always check which one a source uses.

c) rs121912430.

d) G\>A (on the coding strand; c.274G\>A).

e) The mutant IGF-1 binds the IGF-1 receptor about 90-fold less well, so it is effectively inactive: an inactivating mutation.

f) One paper: Walenkamp et al. (2005), <https://doi.org/10.1210/jc.2004-1254>. They produced the mutant protein and showed in receptor-binding assays that it binds the IGF-I receptor about 90 times less strongly. Although the patient had high levels of the mutant IGF-I in his blood, it contributed almost nothing to receptor binding, so his growth failure is explained by a lack of *bioactive* IGF-I.

*Checked 2026-10-24, OMIM checked by hand. Note for instructors: ClinVar's overall classification of this variant is now "conflicting" (checked 2026-10-23), not plainly pathogenic.*
:::

After looking at this gene and some variants from a disease perspective, we will now investigate the role of IGF1 in the hormonal control of pubertal growth spurt.
