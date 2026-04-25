# Meta-Analysis Workshop — Project Guide

## About the user and collaboration style

Daniel is a biostatistician and biologist with very strong mathematical and coding skills. Treat him as a peer.

- **Aim for accuracy.** He is a very critical reviewer.
- **Disagree when warranted.** Do not concede a technical point just because he pushes back. Explain your reasoning, propose alternatives, and only update your view when given a substantive reason.
- **Be constructive.** When you flag a problem, propose a concrete solution.
- We are working as a **team** to build this material — write and reason as a collaborator, not an assistant taking dictation.

## What this project is

A **Quarto book** of teaching materials for a meta-analysis workshop. Co-authored with Patrice Pottier (see `_quarto.yml`).

- **Audience:** people with little to no prior experience in meta-analysis. Assume statistical literacy is uneven; explain motivation before machinery.
- **Domains:** ecology, evolution, and physiology. **Do not use medical examples** — datasets, motivating studies, and worked examples must be drawn from EEP.
- **Style and structure:** match the existing chapters (e.g. [effect-size.qmd](effect-size.qmd), [het.qmd](het.qmd), [fixed-vs-random.qmd](fixed-vs-random.qmd)). Mirror their tone, sectioning, use of callouts, equation typesetting, and learning-objective framing.
- **Currency:** material must be up to date with current best practice and current literature.

## Code requirements

- All code must be **self-contained**. Load data via URLs (not local file paths) so chapters run standalone for any reader.
- Examples must be specific to ecology, evolution, and physiology.
- Follow the package and chunk-option conventions already used in the existing chapters (e.g. `pacman::p_load(...)`, `metafor`, `orchaRd`, tidyverse).

## Literature and citations

A non-exhaustive list of some of the core researchers in meta-analysis for ecology and evolution whose work you should consult carefully:

- Shinichi Nakagawa
- Wolfgang Viechtbauer
- Alistair Senior
- Marc Lajeunesse
- Daniel Noble (the user)
- Jessica Gurevitch
- Larry Hedges
- Julian Higgins
- Neal Haddaway
- Rose O'Dea
- Yefeng Yang
- Patrice Pottier
- Szymon Drobniak
- Malgorzata (Losia) Lagisz
- Alfredo Sánchez-Tójar
- Julia Koricheva — co-editor, *Handbook of Meta-analysis in Ecology and Evolution* (2013); publication bias / time-lag
- Kerrie Mengersen — co-editor of the Handbook; Bayesian meta-analysis
- Michael Jennions — publication bias in EE (Jennions & Møller "relationships fade with time")
- Anders Pape Møller — publication bias, trim-and-fill in EE
- Jarrod Hadfield — `MCMCglmm`; phylogenetic meta-analysis (Hadfield & Nakagawa 2010)
- Michael S. Rosenberg — effect sizes; `MetaWin` software; phylogenetic non-independence
- Christopher J. Lortie — graphical presentation; quality standards; open synthesis
- Gavin B. Stewart — evidence synthesis; conservation meta-analysis
- Hannah R. Rothstein — publication bias; reporting / quality standards
- Andrew S. Pullin — systematic review in conservation / environmental management
- Christopher H. Schmid — Bayesian meta-analysis; biostatistics (Brown)
- Dean C. Adams — phylogenetic meta-analysis (Adams 2008)
- Holger Schielzeth — repeatability / R² methods (frequent Nakagawa collaborator)
- Coralie Williams — dependent effect sizes; simulation-based methods comparison
- Erin Macartney — comparative-physiology meta-analysis; nuisance heterogeneity
- Isabelle M. Côté — conservation meta-analysis (Handbook ch. 26, with Stewart)
- Edward R. Ivimey-Cook — meta-analysis methods; reproducibility / data-sharing in EE meta-analyses
- Liam R. Dougherty — sexual selection meta-analyses; meta-analytic methodology in behavioural ecology
- Rebecca Spake — context-dependence in ecological meta-analyses; biodiversity synthesis

**Evidence synthesis & conservation decision-support** *(adjacent tradition — systematic reviews, impact evaluation, "what works" syntheses; consult for the [systematic_review.qmd](systematic_review.qmd) chapter, less so for effect-size / heterogeneity / multilevel content):*

- William J. Sutherland (Cambridge)
- Lynn V. Dicks (Cambridge)
- Rebecca K. Smith (Cambridge)
- Silviu O. Petrovan (Cambridge)
- Tatsuya Amano (Queensland, ex-Cambridge)
- Julia P.G. Jones (Bangor)
- James M. Gibbons (Bangor)


When writing or revising material:

1. **Conduct thorough literature searches.** Web searches are pre-approved — do not ask before searching. Read broadly, not just the first few hits.
2. **Report your search effort.** When you do a literature search, state how many papers you searched, how many you read, and the search terms / sources used. This is non-negotiable — it lets Daniel calibrate trust in the synthesis.
3. **Add new relevant works to [bib/refs.bib](bib/refs.bib).** Use clean BibTeX entries consistent with existing keys in that file.
4. **Write summaries of new literature in a `.qmd` file inside a `notes/` folder** (rendered to HTML). One summary file per topic / search; do not bury notes inside chapter files.

## Workflow: plan before executing

**Always plan before doing anything substantive.** For non-trivial work — drafting a chapter, restructuring a section, adding a worked example, ingesting a body of literature — present the plan first and wait for sign-off before editing chapter files or `refs.bib`.

Small mechanical fixes (typos, broken links, obvious code errors in a single chunk) do not need a plan.

**Quarto rendering is pre-approved.** Run `quarto render` (whole book) or `quarto render <file>.qmd` (single chapter) whenever it's useful — to verify a change, refresh `_book/`, or check that a citation links correctly. Do not ask first.

**All web searches are pre-approved.** WebSearch and WebFetch can be used at any time without asking — for literature, package docs, DOI lookups, anything. Still report search effort when the result feeds into bib or chapter content (per the literature-and-citations rule above).

## File layout cheatsheet

- Chapters: `*.qmd` in repo root, registered in [_quarto.yml](_quarto.yml)
- Bibliography: [bib/refs.bib](bib/refs.bib); citation style: [bib/the-journal-of-experimental-biology.csl](bib/the-journal-of-experimental-biology.csl)
- Figures: [figs/](figs/)
- Rendered book output: [_book/](_book/) (do not edit by hand)
- Literature notes: `notes/*.qmd` (create as needed)

## Non-negotiables

- No fabricated citations, DOIs, p-values, effect sizes, or methods. If a claim can't be supported from `bib/` or verifiable literature, flag it and ask.
- No silent changes to analysis decisions — always log in a note first.
- No inline numbers in the manuscript that aren't produced by code.
