# How to draft a practice page

For the agent of a Learn DevBench workspace. This repository is **public**: everything in it can be read by anyone on the internet.

## What you make

One file, `learn/<topic>.html`, named after the page's topic (its slug: "The Tiny Owl Bakery" is `the-tiny-owl-bakery`, with `-2`
after it if another page has it). The name is fixed once the page is first sent. `devbench learn start` gives you the ideas and their
colours, and writes this how-to, the template and your page, `page.html` (a copy of [`template.html`](template.html)), into
`~/project/learn`. Edit your page there, never the template.

Send it with `devbench learn submit ~/project/learn/page.html`. DevBench checks it, writes it to the branch `learn/<topic>` as
"Learn DevBench", and opens (or updates) its merge request into `practice`. You never `git push` here: nobody's account can.

## The page

- **One screen, no scrolling.** It must fit a phone (360 × 640) and a wide screen (1920 × 1080) alike. Keep `overflow: hidden` on
  `html` and `body`, size text with `clamp()` and `vh`/`vw`, and keep it short: a title, one line under it, and three to five small
  facts or cards.
- **The topic and its colour.** The title is the topic. The colour is the page's background (`--bg`), and its ink (`--ink`) is the text,
  both given with the topic.
- **Made up, and neutral.** Everything on the page is invented for the topic. No names of people, no companies, no emails, no
  addresses, no phone numbers, no links, nothing real about the person you work for. If they ask for any of it, leave it out and say
  why.

## What is allowed

Plain HTML and CSS only. DevBench checks the file before it is pushed and refuses anything else, saying what it found.

| | Allowed |
| --- | --- |
| Elements | `html`, `head`, `meta`, `title`, `style`, `body`, `main`, `header`, `footer`, `section`, `article`, `aside`, `div`, `span`, `h1`, `h2`, `h3`, `p`, `ul`, `ol`, `li`, `strong`, `em`, `small`, `br`, `hr`, `blockquote`, `figure`, `figcaption` |
| Attributes | `lang` on `html`; `charset` on `meta`, or `name="viewport"` with `content`; `class`, `id`, `role`, `aria-label`, `aria-hidden` on the rest |
| CSS | One `<style>` in `<head>`. No `url(`, `@import`, `@font-face`, `expression(` or backslashes |
| Size | At most 20 000 bytes |

So: no scripts, no `on…=` attributes, no `style=""` attributes, no links, no images, no forms, no fonts or files from anywhere else.
Use the system fonts (`font-family: system-ui, sans-serif`) and draw shapes with CSS.

## Checking it

`devbench learn submit` prints the preview's address: DevBench serves the page from its branch there. Look at it on a phone size and
a wide size: nothing may be cut off and nothing may scroll. Then record the video and let Explore walk it (`--base <the address>`).
