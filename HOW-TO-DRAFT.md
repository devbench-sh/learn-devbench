# How to draft a practice page

For the agent of a Learn DevBench workspace. This repository is **public**: everything in it can be read by anyone on the internet.

## What you make

One file, `learn/<number>.html`, where `<number>` is your Learn DevBench workspace's number. DevBench gives it to you with the topic
and the colour. Make it on the branch `learn/<number>` and open a merge request into `practice`. Never push to `main` or `practice`.

Start from [`template.html`](template.html): copy it to `learn/<number>.html` and fill it in.

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
| CSS | One `<style>` in `<head>`. No `url(`, `@import`, `@font-face` or `expression(` |
| Size | At most 20 000 bytes |

So: no scripts, no `on…=` attributes, no `style=""` attributes, no links, no images, no forms, no fonts or files from anywhere else.
Use the system fonts (`font-family: system-ui, sans-serif`) and draw shapes with CSS.

## Checking it

Open the preview DevBench makes of your branch, on a phone size and a wide size: nothing may be cut off and nothing may scroll.
Then record the video and let Explore walk it, as for any change.
