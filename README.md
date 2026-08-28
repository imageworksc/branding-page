# Branding & Graphic Design Services — ImageWorks Creative

Landing page for ImageWorks Creative's branding and graphic design service.
Published at <https://imageworksc.github.io/branding-page/>.

## Files

    index.html    the markup, and nothing else
    styles.css    every rule on the page
    script.js     the one behaviour that needs a script

Nothing is inline. No `<style>` block, no `style` attribute, no `<script>`
body. The one exception is the JSON-LD in the head, which is structured data
rather than behaviour — moved to an external file, crawlers would not read it.

The webfont and the icon set are still embedded: Plus Jakarta Sans as a base64
`@font-face` in the stylesheet, and the icons as an SVG symbol sheet at the top
of the body. The page makes no external network request.

## Scope

The page carries the five sections of the source copy and nothing else:

1. Hero — the headline, the intro paragraph, two calls to action, and the
   brand board
2. What Is Branding? — the definition, then "it's bigger than a logo"
3. Branding & Graphic Design, Handled In-House — the four service families and
   everything listed under each
4. Nearly Three Decades of Brand Work — the three trust signals and the
   founding year
5. Let's Talk About Your Brand — the closing call

There is no site header and no footer: the page is the article, and the chrome
belongs to whatever it gets placed into.

No section, statistic, testimonial, or FAQ beyond that copy belongs here.
Anything added later needs to come from the client, not from the design.

## The stylesheet

Two things are kept apart inside `styles.css`. The first and larger part is the
design system carried over from
[Custom-Web-Design](https://github.com/imageworksc/Custom-Web-Design) — tokens,
the 2px corner, the card recipe, the bands. **Fix that part upstream and carry
it across, not here,** or the two pages drift apart. This page's own block
follows it, prefixed `bd-` and `bk-`.

Some of the carried-over system is now unused — the rules for the process
flow, the portfolio marquee, the comparison columns, the FAQ and the stats,
whose sections this page does not have. They are left in place rather than
pruned piecemeal; carrying the system whole is what keeps it a system.

## The script

Only the entrance reveal needs JavaScript, because it has to know when a
section comes into view. The file it was split out of carried six more
routines — the sticky header, the dropdown menu, the process rail, the FAQ
accordion, the counting stats and the anchor scrolling — and none of them has
anything left to act on.

Everything else that moves is CSS: the brand board's five loops, the hover
states, and the marker strokes under the definition.

## Before this goes live

Every call to action points at `/contact` and every portfolio link at
`/portfolio`, matching the source copy. Confirm those are the real routes on
the production site.
