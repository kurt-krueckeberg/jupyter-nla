# TODO

## shorten menu items

I have shorten the top-level navigation text using "- title:". This 
is a suggested pattern of changes for the "children:" "-file: " entries:

- title: 1798 Petition
- title: 1798 Report
- title: 1799 Land Assignment
- title: 1800 Purchase Letter

## Check for corrupt converted .md file

Tables were used to display side-by-side some transliterations and translations. During the conversion process
from .adoc to .md, some of these tables were corrupted and some do not fit in the narrower content column of
Jupiter Book 2. A case by case decision will have to be made on each of thesA case by case decision will have to be made on each of thesee

## Two Level Navigation Structure

Sorry, I made a mistake. Let me retry. Instead of the current navigation

- file: 1237/index.md
  title: Krückeberg Lot Enlargement
  children:
    - file: 1237/cover.md
    - file: 1237/narr-timeline.md
    - file: 1237/contents-list.md
      children:
        - file: 1237/doc1.md
        - file: 1237/doc2.md
        
I would do this

  - file: 1237/contents.md
  title: Krückeberg Lot Enlargement
  children:
    - file: 1237/cover.md
    - file: 1237/narr-timeline.md
    - file: 1237/doc1.md
    - file: 1237/doc2.md

The contents-list-and-intro-pages.md page would become the top-level menu item
and the documents it referenes would become its children, along with the
cover page (and perhaps and overview or introduction page). I would either
eliminate index.md or make it the intro.md page, and then in
contents-list-and-intro-pages.md, which has a list-table that reflects the Designation Actorum
and has markdown links to the ccase file's documents, I would have an
unordered list of one or two items consisting of links to cover.md and, if
it exists, to intro.md.

This gives a two level structure:

```text
Krückeberg Lot Enlargement (Contents list page)
  Cover
  Narrative Timeline
  Document 1
  Document 2
  ...
```

And contents.md becomes the real case-file landing page, containing:

```text
# Krückeberg Lot Enlargement

Brief explanation of the case file.

## Introductory Pages

- [Cover](cover.md)
- [Narrative Timeline](narr-timeline.md)

## Designatio Actorum

| No. | Document | Date |
| --- | --- | --- |
| 1 | [Jobst Heinrich Krückeberg Petition](doc1.md) | 29 May 1798 |
| 2 | [Report ...](doc2.md) | ... |
```

- Only one nesting level is used.
- index.md can be eliminate or renamed intro.md
- the navigation is still built from myst.yml.

Furthermore, the 2nd level navigation can come from short "title:" text
which can comes from come patterns found across the case files--petition,
office report, offical reply, etc.
