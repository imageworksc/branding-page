# Branding & Graphic Design Services — ImageWorks Creative

Single-file landing page for ImageWorks Creative's branding and graphic design
service. Published at <https://imageworksc.github.io/branding-page/>.

## What's here

`index.html` is the whole page — markup, stylesheet, icon set, and scripts in
one document, with the Plus Jakarta Sans webfont and the logos inlined as data
URIs. It makes no external network request.

## Scope

The page carries the five sections of the source copy and nothing else:

1. Hero — the headline, the intro paragraph, two calls to action, and the
   brand-kit visual
2. What Is Branding? — the definition, then "it's bigger than a logo"
3. Branding & Graphic Design, Handled In-House — the four service families and
   everything listed under each
4. Nearly Three Decades of Brand Work — the three trust signals and the
   founding year
5. Let's Talk About Your Brand — the closing call

No section, statistic, testimonial, or FAQ beyond that copy belongs on this
page. Anything added later needs to come from the client, not from the design.

## Design system

The stylesheet is the one from
[Custom-Web-Design](https://github.com/imageworksc/Custom-Web-Design), carried
over unchanged: the same brand tokens, the same 2px corner, the same card
recipe, the same white / tint / CTA bands, and the same sticky header and
footer. Only the pieces this page needs — the service chips, the brand kit, the
trust grid, and four added service icons — are declared in a second `<style>`
block, all prefixed `bd-`.

**Don't edit the shared stylesheet here.** Fixes belong upstream in
Custom-Web-Design, then get carried across, or the two pages drift apart.

Three sets of rules from that stylesheet were dropped rather than shipped
unused, since their data URIs are most of the page weight: `.mc-shot` (87KB)
and `.work-shot--1..8` (~200KB), the screenshots behind the web-design page's
browser mockup and portfolio marquee.

## Before this goes live

Every call to action points at `/contact` and every portfolio link at
`/portfolio`, matching the source copy. Confirm those are the real routes on
the production site.
