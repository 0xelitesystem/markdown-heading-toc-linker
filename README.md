# Markdown TOC Generator

Generate a linked table of contents from markdown headings, entirely in your browser.

**Live demo:** https://0xelitesystem.github.io/markdown-toc-generator/

## Use

1. Paste your markdown into the input box. The table of contents updates as you type.
2. Pick the minimum and maximum heading levels to include (for example, H2 through H3).
3. Choose the list style (bulleted with `-` or `*`, or numbered), the indent width, and whether to emit anchor links.
4. Click **Copy TOC** and paste the result at the top of your document.

The generator parses ATX headings (`## Heading`) and setext headings (text underlined with `===` or `---`). It skips anything inside fenced code blocks (` ``` ` or `~~~`), so commented `# lines` in shell snippets are not mistaken for headings. Anchor slugs follow the GitHub convention: lowercased, spaces turned into hyphens, punctuation stripped, and duplicate headings suffixed with `-1`, `-2`, and so on.

## Why this exists

Most online TOC tools paste your document into a server you do not control, wrap a one-page utility in a framework and a tracker, or quietly fail on code blocks and duplicate headings. This is one HTML file with no build step, no dependencies, no analytics, and no network calls. Open the source and read every line. It is MIT licensed, so copy it, fork it, or host it yourself.

## Privacy

Everything runs in your browser. Your markdown is never uploaded, logged, or sent anywhere. There are no cookies, no analytics, and no network requests of any kind. You can disconnect from the internet and the tool still works.

## Run locally

```
git clone https://github.com/0xelitesystem/markdown-toc-generator.git
cd markdown-toc-generator
```

Then open `index.html` in any browser. Or serve it locally:

```
python -m http.server
```

and visit `http://localhost:8000`.

## Build

There is no build. It is a single self-contained `index.html` with inline CSS and JavaScript. No bundler, no package manager, no dependencies.

## License

MIT. See [LICENSE](LICENSE).

## Related

- [jwt-inspector](https://github.com/0xelitesystem/jwt-inspector)
- [eeat-signals-reference](https://github.com/0xelitesystem/eeat-signals-reference)
