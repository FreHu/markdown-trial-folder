# The markdown trial folder

A real folder of markdown, to open in markdown viewers and compare what each does with it: what breaks when files link to each other, images sit beside them, and paths have to be resolved. Everything here is made up.

| Path | What it tries |
| --- | --- |
| `README.md` | A README as projects write it: a centred logo in HTML, a row of remote badges, a relative screenshot, a contents list linking headings here and in other files, code in bash, PowerShell, TypeScript, YAML and a `diff`. |
| `docs/setup.md` | TOML front matter (Hugo), images beside and above the file, code titles and highlighted lines as VitePress and Docusaurus write them, a dozen languages, a block with no language and one with an unknown one, a very long line and a one-line paragraph. |
| `docs/links.md` | Every kind of link and image path: beside, up, from the root, to a heading, with a space, an upper-case extension, a folder, a missing file and heading, a query, the wrong case, reference-style, `mailto:`, `tel:`, `file:`. |
| `docs/gitlab.md` | GitLab's own syntax: `[[_TOC_]]`, the `>>>` quote, colour chips, a JSON table it can sort and filter, issue and merge request references, inline diff. |
| `docs/azure-devops.md` | Azure DevOps wiki syntax: `[[_TOC_]]`, `::: mermaid`, `[[_TOSP_]]`, work items and people. |
| `docs/json-front-matter.md` | Front matter written as JSON. |
| `data/stock.md` | A table of 72 stock movements: the one to sort, filter, total and chart. |
| `data/query-log.md` | A database query log as a person keeps one while working (about 200 KB, 58 entries): each a heading with the time, connection and what was asked, the SQL, a result table or an error, and a row count. It holds JSON cells cut short with "…", a base64 cell wrapped every 76 characters and cut short, and writes whose SQL carries JSON as base64 (`from_base64('…')`: SQL blocks up to 72 KB, single lines up to 48 KB, the largest written twice), the JSON holding JSON and HTML in its strings. Where damaged data turns up in real markdown. |
| `CHANGELOG.md` | A long changelog in Keep a Changelog style, for the outline, navigation and speed. |
| `examples/` | One file per family of syntax (CommonMark and tables, GitHub's extras, math, Mermaid, other diagrams, Obsidian, documentation sites) and a table to explore; links and embeds in them (the Obsidian floor plan, Hugo's `/img/zone-c.png`) resolve to real files here. |
| `assets/`, `img/`, `docs/img/` | The images the files point to. |

Open the folder as a whole where a tool can (a folder opened in a viewer, a VS Code workspace, an Obsidian vault), so links between files have somewhere to go.
