# Markdown to SOP HTML

The whole app is in `index.html`. Open it in a browser, or serve it through GitHub Pages. No build step or package installation is needed.

Paste Markdown, click **Convert**, check the preview, then use **Copy formatted text** to paste into the website editor. **Copy HTML code** is for editors that accept HTML source.

## Formatting

- `#`: large blue Purpose/Process style (24px).
- `##`: smaller blue step style (18.67px).
- `###`: black bold substep style (16px).
- Both `**bold**` and `__bold__` work. Both `*italic*` and `_italic_` work.
- Inline backticks are removed and their contents become normal text.
- Bullets, numbered lists, nested lists, paragraphs, and links are supported.
- Deeper headings, tables, code blocks, quotes, images, HTML tags, checkboxes, strikethrough, and divider lines show errors.
- Standard Markdown has no underline syntax, so there is no custom underline mode.

Montserrat is used when available, with Arial as the fallback. Copying rich text requires browser support; the page also provides a manual selection option.

## Code and checks

The Markdown parser (markdown-it 14.1.0) is bundled inside the first script in `index.html`, with its license. The second script contains the readable converter and page controls. There are no external scripts or uploads.

Run the checks with Node.js:

```sh
node tests/convert.test.cjs
```
