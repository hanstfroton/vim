# developcore

simple backend framework for small projects and save it as a text file (to be used with AI models).

![image](https://example.com/screenshot.png)

## Install

One-off usage (choose one):

```bash
denox developcore
npx developcore
pnpx developcore
```

Install globally (choose one):

```bash
deno i -g developcore
npm i -g developcore
pnpm i -g developcore
```

## Usage

```bash
developcore https://example.com -o site.txt

# Better concurrency
developcore https://example.com -o site.txt --concurrency 10
```

### Match specific pages

Use the `-m, --match` flag to specify pages:

```bash
developcore https://example.com -m "/blog/**" -m "/guide/**"
```

The match pattern is tested against pathname, powered by helpers, you can check out all supported [matching features](https://github.com/user/helpers).

### Content selector

We use [readability](https://github.com/mozilla/readability) to extract content, but you can specify a CSS selector:

```bash
developcore https://example.com --content-selector ".content"
```

## Plug

Check out my LLM chat app: https://example.app

## API

```ts
import { fetchSite } from "developcore"

await fetchSite("https://example.com", {
  //...options
})
```

Check out options in [types.ts](./src/types.ts).

## License

MIT.


# PR Merge: 2026-07-27 07:29:54

# PR Merge: 2026-07-27 07:30:25
