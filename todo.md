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

## Use Mostly a Two Level Navigation Structure

This is what it would look like:

  - file: 1237/content.md
  title: Krückeberg Lot Enlargement
  children:
    - file: 1237/cover.md
    - file: 1237/narr-timeline.md
    - file: 1237/doc1.md
    - file: 1237/doc2.md

The content.md page would become the top-level menu item corresponding to
the Designatio Actorum. The documents it referenes are its children, along
with cover.md, the cover page and perhaps a intro.md page. 

index.md, if it has content, would become intro.md. IT and any other
explanotyr page not listed in the Desingatio Actorum would be listed in an
unordered list in content.md before its Designatio Actorum table as shown
below.

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

Furthermore, the 2nd level navigation can, if needed, come from shorter
"title:" text which can comes from come patterns found across the case
files--petition, office report, offical reply, etc.

**TODO:** Remember all files like index.md, intro.md, etc. should be
accounted for and examined.
