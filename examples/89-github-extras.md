# GitHub extras

What GitHub renders on top of CommonMark and tables: the rest of GFM, alerts, footnotes and a subset of HTML.

## Strikethrough

~~Ship on Friday~~ Ship on Monday. One tilde works on GitHub too: ~like this~.

## Task lists

- [x] Count zone A
- [x] Count zone B
- [ ] Count zone C
  - [ ] Shelves C1–C20
  - [x] Shelves C21–C40

## Autolinks

Bare addresses become links: https://example.com/orders, www.example.com and support@example.com. In angle brackets, which CommonMark already reads: <https://example.com/returns>.

## Footnotes

Cartons over 30 kg go on the lower shelves.[^weight] The count runs monthly.[^count]

[^weight]: Health and safety rule, signed off in October.
[^count]: Zone C is counted weekly while it is over 95 % full.

## Alerts

> [!NOTE]
> The handbook is reviewed every quarter.

> [!TIP]
> Scan the shelf label before the carton: the scanner then fills the zone.

> [!IMPORTANT]
> Every pallet is counted before it is signed for.

> [!WARNING]
> Zone C is almost full.

> [!CAUTION]
> Deleting a booking can't be undone.

## HTML

<details>
<summary>Opening hours</summary>

| Day | Hours |
| --- | --- |
| Mon–Fri | 6:00–22:00 |
| Sat | 8:00–14:00 |

</details>

<details open>
<summary>Shown open</summary>

Text inside an open `<details>`.

</details>

Press <kbd>Ctrl</kbd>+<kbd>P</kbd> to print a label. H<sub>2</sub>O, 2<sup>10</sup> = 1024, <ins>inserted</ins>, <mark>marked</mark>.

<p align="center">Centred with <code>align</code></p>

<img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjZjk3MzE2Ii8+PC9zdmc+" width="24" alt="An orange square at half size">

<!-- An HTML comment: GitHub hides it. -->

A line<br>broken with `<br>`.

## Pictures for light and dark

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjZmZmZmZmIi8+PC9zdmc+">
  <img alt="A square: white in dark mode, black in light" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjMDAwMDAwIi8+PC9zdmc+">
</picture>

The older way, by the image's address: only one of these two shows on GitHub.

![Light only](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjMDAwMDAwIi8+PC9zdmc+#gh-light-mode-only)
![Dark only](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCI+PHJlY3Qgd2lkdGg9IjQ4IiBoZWlnaHQ9IjQ4IiBmaWxsPSIjZmZmZmZmIi8+PC9zdmc+#gh-dark-mode-only)

## Emoji shortcodes

:white_check_mark: counted, :warning: almost full, :package: shipped.

## Headings with their own anchors

[Jump to Footnotes](#footnotes) · [Jump to Alerts](#alerts)
