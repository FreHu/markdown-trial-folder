+++
title = "Setup in detail"
weight = 10
draft = false
+++

# Setup in detail

Front matter here is TOML, as Hugo writes it. Back to the [README](../README.md), or its [Usage section](../README.md#usage).

![Flow, from beside this file](img/flow.png)

![The logo, one folder up](../assets/logo.png)

## Install

```sh
git clone https://github.com/shelfwise/shelfwise.git
cd shelfwise
npm ci
```

## Configure

A code block with a title and highlighted lines, as VitePress writes it:

```ts{2,4} [shelfwise.config.ts]
export default {
  zones: ['A', 'B', 'C'],
  scanner: 'zebra',
  syncEvery: '5m',
};
```

The same, as Docusaurus writes it:

```ts title="shelfwise.config.ts" {2,4}
export default {
  zones: ['A', 'B', 'C'],
  scanner: 'zebra',
  syncEvery: '5m',
};
```

## Code in many languages

```json
{ "zone": "C", "shelves": 40, "full": 0.99 }
```

```python
def missing(expected: set[str], scanned: set[str]) -> set[str]:
    return expected - scanned
```

```sql
SELECT zone, SUM(quantity) FROM movement GROUP BY zone;
```

```go
func Missing(expected, scanned map[string]bool) []string {
	var out []string
	for k := range expected {
		if !scanned[k] {
			out = append(out, k)
		}
	}
	return out
}
```

```rust
fn missing(expected: &[&str], scanned: &[&str]) -> Vec<String> {
    expected.iter().filter(|e| !scanned.contains(e)).map(|e| e.to_string()).collect()
}
```

```csharp
var missing = expected.Except(scanned).ToList();
```

```dockerfile
FROM node:22-alpine
COPY . /app
RUN npm ci --omit=dev
CMD ["node", "/app/server.js"]
```

```ini
[scanner]
model = zebra
timeout = 30
```

```xml
<zone name="C" shelves="40"/>
```

```html
<button class="count">Count zone C</button>
```

```css
.count { background: #f97316; }
```

```text
A block in plain text, with a very long line that runs well past the width of any reasonable window so the viewer has to decide whether to wrap it or scroll it sideways.
```

```
A block with no language at all.
```

```unknownlang
A block in a language nobody knows.
```

## A long line of prose

This paragraph has no line breaks in it at all, because that is how many people write markdown: one paragraph is one very long line, and the viewer is expected to wrap it to the window, keep links and `inline code` working across the wrap, and not lose the reader's place when the window is resized.
