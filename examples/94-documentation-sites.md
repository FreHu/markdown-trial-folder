# Documentation sites

What documentation generators and Pandoc add: admonitions, attributes, definition lists, tabs, includes.

[[toc]]

[TOC]

## Containers (VitePress, Docusaurus, markdown-it, Pandoc)

::: tip
Scan the shelf label first.
:::

::: warning Ladder needed
Zone C's top shelves.
:::

:::note[Docusaurus with a title]
Counting starts at 6:00.
:::

::: details Opening hours
Mon–Fri 6:00–22:00.
:::

## Admonitions (MkDocs Material, Python-Markdown)

!!! note
    The count runs monthly.

!!! warning "Almost full"
    Zone C is over 95 %.

??? tip "Folded until opened"
    Count left to right.

???+ info "Open, can be folded"
    Bring a charged scanner.

## Tabs (MkDocs Material)

=== "Scanner"

    Scan the shelf, then the carton.

=== "By hand"

    Write the shelf and carton on the count sheet.

## Attributes (Pandoc, kramdown, markdown-it-attrs)

## Receiving {#receiving .important}

A paragraph with a class.
{: .lead }

[A button](https://example.com/count){.button target="_blank"}

## Definition lists (Pandoc, PHP Markdown Extra, kramdown)

SKU
: Stock keeping unit, one per product variant.

Zone
: A group of shelves counted together.
: Named by a letter.

## Sub- and superscript (Pandoc, markdown-it)

H~2~O and 2^10^ = 1024.

## Abbreviations (PHP Markdown Extra, MkDocs)

The SKU is on every label.

*[SKU]: Stock keeping unit

## Inserted and marked (markdown-it)

++Inserted text++ and ==marked text==.

## Includes and snippets

--8<-- "shared/opening-hours.md"

{!shared/opening-hours.md!}

## Hugo shortcodes

{{< figure src="/img/zone-c.png" caption="Zone C" >}}

{{% notice warning %}}
Mind the ladder.
{{% /notice %}}

## MDX (Docusaurus, Next.js)

import Tabs from '@theme/Tabs';

<Tabs>
  <TabItem value="scanner" label="Scanner">Scan the shelf, then the carton.</TabItem>
</Tabs>

## Keyboard keys (pymdownx.keys)

++ctrl+p++ prints a label.

## Critic markup (pymdownx.critic)

The count is {--weekly--}{++monthly++}. {>>Changed in October.<<} {==Zone C==} stays weekly.
