---
title: Every kind of link
---

# Every kind of link

What a folder of markdown links to, and what a viewer has to resolve.

## To other files

- Beside this one: [setup](setup.md), and with `./`: [setup](./setup.md)
- One folder up: [README](../README.md)
- To a heading in another file: [Install](setup.md#install), [Usage](../README.md#usage)
- To a heading with spaces and punctuation: [Code in many languages](setup.md#code-in-many-languages)
- From the folder's root, as GitHub reads a leading slash: [README](/README.md), [setup](/docs/setup.md)
- To a file with a space in its name: [a picture](../assets/my%20image.png), and unescaped: [a picture](<../assets/my image.png>)
- To a file with an upper-case extension: [UPPER.PNG](../assets/UPPER.PNG)
- To a folder, not a file: [the examples](../examples/), [docs](./)
- To data, not markdown: [the stock table](../data/stock.md)
- To a file that does not exist: [missing](nowhere.md), [missing heading](setup.md#no-such-heading)
- With a query: [setup](setup.md?plain=1)
- In a different case than on disk: [SETUP](SETUP.md)

## Images by every route

![Beside this file, in a subfolder](img/flow.png)

![One folder up](../assets/screenshot.png)

![From the root](/assets/logo.png)

![With a space](../assets/my%20image.png)

![Upper-case extension](../assets/UPPER.PNG)

![Missing](../assets/nowhere.png)

![Remote](https://img.shields.io/badge/remote-image-blue)

## Reference-style

[Setup][setup], [the changelog][changelog], and [the 1.0 release][v1].

[setup]: setup.md
[changelog]: ../CHANGELOG.md
[v1]: ../CHANGELOG.md#100---2025-03-01

## On this page

- [Back to the top](#every-kind-of-link)
- [To other files](#to-other-files)

## Outside

- A web page: [CommonMark](https://commonmark.org)
- Mail: [support](mailto:support@example.com)
- A phone number: [call](tel:+420123456789)
- A Windows path written by hand: [C:\Users\shared\stock.md](file:///C:/Users/shared/stock.md)
