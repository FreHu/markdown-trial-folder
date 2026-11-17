---
title: GitLab's markdown
---

# GitLab's markdown

[[_TOC_]]

## Multi-line quote

>>>
A quote written as GitLab allows,
across several lines,

with a paragraph break inside.
>>>

## Colour chips

The brand colour is `#F97316`, the warning `RGB(234, 179, 8)` and the text `HSL(222, 47%, 11%)`.

## JSON table

GitLab draws this block as a table a reader can sort and filter.

```json:table
{
  "fields": [
    { "key": "zone", "label": "Zone", "sortable": true },
    { "key": "shelves", "label": "Shelves", "sortable": true },
    { "key": "filled", "label": "Filled", "sortable": true }
  ],
  "items": [
    { "zone": "A", "shelves": 120, "filled": "87 %" },
    { "zone": "B", "shelves": 96, "filled": "64 %" },
    { "zone": "C", "shelves": 40, "filled": "99 %" }
  ],
  "filter": true,
  "caption": "Stock by zone"
}
```

## Diagrams GitLab draws

```plantuml
Bob -> Alice : count zone C
```

## References GitLab links

Issue #42, merge request !17, @logistics-team, the commit 3d2782a, the milestone %"2026-Q4" and the label ~"zone C".

## Inline diff

The shelf moved from {- C12 -} to {+ C14 +}.

## Front matter as JSON

See [json-front-matter.md](json-front-matter.md).
