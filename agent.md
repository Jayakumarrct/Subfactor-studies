# Agent Playbook: Subfactor Notes Project

## Mission & Audience
- Deliver an expandable set of lecture notes that guide readers from graduate foundations to active research problems in subfactor theory.
- Spotlight principal graphs and Bratteli diagrams as the unifying graphical language of the notes.
- Write for two audiences simultaneously: newcomers who need intuition and basic examples, and researchers who expect precise statements, structural theorems, and references.

## Core Outcomes
- A vertically structured manuscript (chapters, sections, subsections) ready for ongoing expansion.
- Every new concept arrives with its characteristic properties, geometric or categorical intuition, and a tiered ladder of worked examples (introductory → intermediate → research-level or open-ended).
- A curated gallery of principal graphs / Bratteli diagrams with TikZ templates that can be expanded in future iterations.

## Macro Roadmap
- **Part 1 – Operator Algebra Foundations**
  - C*- and W*-algebras, Hilbert spaces, bounded operators, von Neumann algebras, factors, traces, commutants.
  - Emphasize characteristic checklists and contrasts (commutative vs non-commutative, finite vs infinite, separable vs non-separable).
- **Part 2 – Jones Index and Standard Invariant**
  - Definition, basic inequalities, tower construction, Temperley–Lieb algebra, standard invariant, paragroups.
  - Worked examples: matrix inclusions, finite group inclusions, the hyperfinite II$_1$ tower, TL planar algebra viewpoint.
- **Part 3 – Graphical Invariants**
  - Principal graphs, dual principal graphs, Bratteli diagrams, fusion rules, Ocneanu’s triple point obstruction, ADE classification.
  - Include algorithms for building graphs from inclusions and a table mapping low-index subfactors to their graphs.
- **Part 4 – Example Atlas**
  - Organize by origin: group-subgroup, quantum groups, planar algebras, small index exotica, connections to conformal nets.
  - For each example: construction sketch, indices, graphs, notable properties, references, potential extensions.
- **Part 5 – Advanced Themes**
  - Connections and flatness, Popa’s reconstruction, paragroup theory, planar algebras, fusion categories, modular data, current research questions.
  - Flag open problems or conjectures for reader exploration.
- **Appendices**
  - Character tables (e.g., $A_n$, small finite groups), notation index, glossary, computational toolbox (FusionAtlas, planar algebra packages), timeline of landmark results.

## Writing Guidelines
- **Vertical Flow**
  - Prefer short paragraphs, blank lines between logical units, and judicious use of lists; avoid dense article-style blocks.
  - Use displayed equations for key identities and keep them separated by blank lines for readability.
- **Characteristics First**
  - Introduce each concept with a bullet or numbered list of defining traits before proofs or consequences.
- **Example Ladder**
  - Standard format: `Introductory Example` → `Intermediate Example` → `Research/Frontier Example` (or open problem). Mark explicitly with headings or environment titles.
- **Notation Consistency**
  - Reuse macros already in the preamble (`\M`, `\N`, `\Hil`, `\B`, etc.). Declare new macros in the preamble before use.
- **Styled Environments**
  - Stick to the colored `definition`, `theorem`, `lemma`, `proposition`, `example` environments already configured. Avoid introducing new box styles unless necessary.
- **Figure Standards**
  - Draw principal/Bratteli diagrams with TikZ. Center figures, leave vertical breathing room (`\vspace` only if spacing needs fine-tuning). Provide captions describing the graph’s origin and index.
- **Referencing & Citations**
  - Insert `\cite{}` placeholders for any external fact. Maintain a TODO list for building `references.bib`.
- **Terminology Callouts**
  - Introduce glossary-style callouts for recurring notions (e.g., “Temperley–Lieb algebra (see Glossary)”) to ease cross-referencing.

## Development Workflow
1. **Planning**
   - Update this playbook or a shared TODO block at the top of the `.tex` file with upcoming sections and example targets.
2. **Drafting**
   - Write in vertical form, with placeholder comments `% TODO:` for missing proofs, diagrams, or references.
   - When introducing diagrams, sketch rough TikZ structure and leave `% TODO: refine figure` notes if time-limited.
3. **Review**
   - Compile via `pdflatex -interaction=nonstopmode` twice. Check for warnings (especially `hyperref` and missing citations).
   - Scan the PDF for vertical spacing, color consistency, and figure alignment.
4. **Integration**
   - Clean up temporary comments once tasks are resolved. Ensure new macros are documented near their introduction.
5. **Version Control**
   - Commit per logical chunk (e.g., “Add definition + examples of Type II$_1$ factors”). Include checklist of addressed TODOs in the message when possible.

## Quality Checklist (per section)
- [ ] Concept introduced with characteristic bullet list.
- [ ] Minimum of two worked examples (aim for three-tier ladder when feasible).
- [ ] Diagram planned or inserted if the concept admits one (especially for principal/Bratteli topics).
- [ ] References or placeholders added for nontrivial claims.
- [ ] Vertical spacing visually clean in compiled PDF.
- [ ] Notation consistent with preamble macros.

## Content Backlog & Priorities
- Expand Part 2 with a gentle derivation of the Jones tower and explicit calculations for $[M_2(\C):\text{diag}(\C,\C)]`.
- Build a dedicated subsection on ADE classification with tables of principal graphs and short narratives for each family.
- Add tutorial-style walkthrough of constructing a Bratteli diagram from an inclusion of AF-algebras.
- Curate a list of “research frontier” examples: Haagerup, extended Haagerup, Asaeda–Haagerup, etc., with brief historical context.
- Assemble appendix entries: character tables for $A_n$, low-rank quantum groups, glossary of recurring symbols.

## Resources & References to Consult
- V. F. R. Jones, “Index for subfactors.”
- S. Popa, “Classification of Subfactors and Their Endomorphisms.”
- D. E. Evans & Y. Kawahigashi, *Quantum Symmetries on Operator Algebras*.
- V. Ostrik, S. Morrison, E. Penneys et al. on planar algebras and small index subfactors.
- FusionAtlas documentation for computational insights.

## Maintenance Notes
- Revisit this playbook whenever scope changes (new appendix, major structural shift, etc.).
- Ensure collaborators (including external agents) read this file before contributing to maintain voice and formatting.
