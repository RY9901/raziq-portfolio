# raziq-portfolio

My personal site. One page, hand-written HTML and CSS.

No framework, no build step, no bundler, no CDN script, no tracking. The only
network request the page makes is to Google Fonts. Clone it and open
`index.html` and you have the whole thing.

## Files

| File | What it holds |
| --- | --- |
| `index.html` | The page. All of the content lives here. |
| `styles.css` | The page's own rules. |
| `tokens.css` | Every colour, font, space and duration, declared once at `:root`. |
| `base.css` | Resets and the rules that apply everywhere. |

No colour or font appears anywhere outside `tokens.css`. To change the palette,
change those tokens and nothing else.

## Running it

Open `index.html` in a browser. That is all it needs.

To serve it over HTTP instead:

```
npx serve .
```

## Design

Cool slate paper, blue-black ink, Hanken Grotesk headings over a Newsreader
serif, IBM Plex Mono for figures only, and one deep magenta held to the primary
button and the focus ring. Surfaces are carried by two rule weights rather than
cards or shadows.

The centre of the page is a table setting my two jobs side by side, because the
record is the argument.

## Constraints I held myself to

- Every colour and font goes through a token at `:root`.
- Body text at 16px or more. Contrast computed from the tokens, not guessed:
  every pair passes WCAG AA, the lowest at 5.06:1.
- `overflow-x: clip` on `html` and `body`; checked for horizontal overflow at
  375px.
- Only `transform` and `opacity` move, and `prefers-reduced-motion` is honoured.
- The page works with scripting off, because there is no script.
- One filled button on the page. Visible `:focus-visible` on everything
  interactive.
- Nothing claimed that I have not actually worked in.

## Licence

The code is free for you to learn from. The content, my name, my record and my
likeness, is mine.
