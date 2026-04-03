---
title: 'SWAT4HCLS26 report: OpenMRS as a reference implementation platform for Electronic Health Records and Clinical Decision Support'
title_short: 'SWAT4HCLS26: OpenMRS as reference implementation platform'
tags:
  - Reference Implementation
  - Electronic Healthcare systems
  - Health standards
  - Teaching Medical Informatics
authors:
  - name: Andra Waagmeester
    orcid: 0000-0001-9773-4008
    affiliation: 1
    role: Writing – original draft
  - name: Stephanie "Ace" Medlock
    orcid: 
    affiliation: 1
    role: Writing – original draft
  - name: Claude Nanjo 
    affiliation: 2
    role: Writing – original draft
  - name: Ronald Cornet
    orcid: 0000-0002-1704-5980
    affiliation: 1
    role: Writing – original draft
affiliations:
  - name: Department of Medical Informatics, AmsterdamUMC, Location AMC Amsterdam, the Netherlands
    index: 1
  - name: University of Utah
    index: 2
    
date: 26 March 2026
cito-bibliography: paper.bib
event: SWAT4HCLS
biohackathon_name: "Biohackathon SWAT4HCLS 2026"
biohackathon_url:   "https://swat4hcls.org/"
biohackathon_location: "AmsterdamUMC"
group: OpenMRS
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/andrawaag/OpenMRS-as-a-Living-Lab
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---


# Introduction

The broad goal for the OpenMRS table is: What steps are needed to use OpenMRS as a resource for reference implementations?

This can be divided into 4 levels:

1. Use OpenMRS as a data source, using its available APIs
This is the easiest one. I will set up an OpenMRS instance that can be used, and provide the URL, some logins, and some instructions. The goal for anyone working on this will simply be to work on whatever demo they want to work on, using the APIs and the fake data provided by this system.

2. Use OpenMRS running locally, so that you can directly access its database
The instructions provided by the OpenMRS community for the newest version (O3) are actually not bad, and I have some detailed notes about how to do this on Linux that I can share with the group. I've never done it on Windows, but it can't be that hard. The goal for anyone working on this will be to come up with instructions for installing the system on Windows, and querying the database (e.g. from Python). This is probably what Claude Nanjo will need to start with.

3. Add a module to OpenMRS
This is the first step toward making modifications to OpenMRS itself. The OpenMRS community provides some "instructions for developers". The goal for anyone working on this will be to follow those instructions (and improve them where needed) with the goal of adding a simple module (I would suggest "add a clickable URL to the patient summary screen" as a good objective for MyFirstModule). This is what will be needed for Claude's goal, if OpenMRS does not already have a module that supports data entry for the data he needs for his idea.

4. Build OpenMRS from source
This is what we'll be working on. This is what you need if you want to change something in OpenMRS, rather than just adding something to it. The goal will be to come up with a set of instructions for how it can be bult from source... preferably in an executable format (e.g. a Makefile).

## Sources:
- https://gitlab.com/ericherman/openmrs-sandbox
- https://gitlab.com/openmrs_education/openmrs-sdk-sandbox



### Contributor Role Taxonomy

A last feature since is minimal support for the Contributor Role Taxonomy (CRediT). You
can specify the role of authors in writing the report with the `role:` field. However,
the authors are responsible for selection the right terms from [CRediT](https://credit.niso.org/).
An example looks like this:

```yaml
authors:
  - name: First Author
    affiliation: 1
    orcid: 0000-0000-0000-0000
    role: Conceptualization, Writing – review & editing
```

### A full examples

A full example then has this structure:

```yaml
authors:
  - name: First Author
    affiliation: 1
    role: Writing – original draft
  - name: Last Author
    orcid: 0000-0000-0000-0000
    affiliation: 2
    role: Conceptualization, Writing – review & editing
affiliations:
  - name: First Affiliation
    index: 1
  - name: ELIXIR Europe
    ror: 044rwnt51
    index: 2
```

# Formatting

This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables

Tables can be added in the following way, though alternatives are possible:

```markdown
Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |
```

This gives:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

## Figures

A figure is added with:

```markdown
![Caption for BioHackrXiv logo figure](./biohackrxiv.png)
```

This gives:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

Figures can be scaled by adding the width or height to the Markdown like this:

```markdown
![Caption for BioHackrXiv logo figure](./biohackrxiv.png){ width=50px }
```

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
