<p align="center">
  <img src="assets/logo.png" alt="Shelfwise logo" width="64">
</p>

# Shelfwise

[![Build](https://img.shields.io/github/actions/workflow/status/shelfwise/shelfwise/ci.yml?branch=main)](https://github.com/shelfwise/shelfwise/actions)
[![npm](https://img.shields.io/npm/v/shelfwise.svg)](https://www.npmjs.com/package/shelfwise)
[![Downloads](https://img.shields.io/npm/dm/shelfwise.svg)](https://www.npmjs.com/package/shelfwise)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![codecov](https://codecov.io/gh/shelfwise/shelfwise/branch/main/graph/badge.svg)](https://codecov.io/gh/shelfwise/shelfwise)

Warehouse stock counts from a phone, synced to one spreadsheet. A made-up project: this README is what a real one holds, so a markdown viewer can be tried on it.

![The count screen](assets/screenshot.png)

## Contents

- [Install](#install)
- [Usage](#usage)
- [Setup in detail](docs/setup.md)
- [Install, in the setup guide](docs/setup.md#install)
- [October's stock movements](data/stock.md)
- [Changelog](CHANGELOG.md)
- [Every kind of link](docs/links.md)

## Install

```bash
npm install shelfwise
```

```powershell
winget install Shelfwise.Shelfwise
```

## Usage

```ts
import { count } from 'shelfwise';

const result = await count({ zone: 'C', shelves: ['C1', 'C2'] });
console.log(result.missing);
```

The config file, `shelfwise.yaml`:

```yaml
zones:
  - name: C
    shelves: 40
    countEvery: week
```

What changed in the API:

```diff
- count(zone, shelves)
+ count({ zone, shelves })
```

## How it flows

![Flow](docs/img/flow.png)

## Contributing

See [the setup guide](./docs/setup.md) and the [changelog](./CHANGELOG.md#unreleased). Questions go to [the discussion board](https://github.com/shelfwise/shelfwise/discussions).

## License

[MIT](LICENSE) © Shelfwise contributors
