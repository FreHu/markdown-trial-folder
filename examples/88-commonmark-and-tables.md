---
title: Warehouse handbook
owner: Logistics
reviewed: 2026-10-30
tags: [warehouse, onboarding]
---

# Warehouse handbook

Plain CommonMark and GFM tables: what every markdown file uses. **Bold**, *emphasis*, _also emphasis_, `inline code`, a [link](https://example.com/handbook "The handbook online") and a hard\
line break.

## Receiving

1. Check the delivery note against the purchase order.
2. Count the cartons.
   - Damaged carton: photograph it before opening.
   - Missing carton: note it on the delivery note.
3. Book the goods in.

> A quote, with a nested one:
>
> > Never sign for a pallet you haven't counted.

---

## Stock by zone

| Zone | Shelves | Filled | Last count |
| :--- | ---: | ---: | :---: |
| A | 120 | 87 % | 2026-11-02 |
| B | 96 | 64 % | 2026-11-09 |
| C | 40 | 99 % | 2026-10-28 |

## Code

```sql
SELECT zone, count(*) AS shelves
FROM shelf
GROUP BY zone;
```

    An indented code block, four spaces in.

Setext heading
--------------

Reference-style [links][handbook] and an image from the data itself:

![A small orange square](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjZjk3MzE2Ii8+PC9zdmc+)

[handbook]: https://example.com/handbook
