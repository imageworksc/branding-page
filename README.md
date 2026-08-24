# Branding & Graphic Design Services — ImageWorks Creative

Single-file landing page for ImageWorks Creative's branding and graphic design
service. Published at
<https://imageworksc.github.io/branding-page/>.

## What's here

`index.html` is the whole page — markup, stylesheet, icon set, and scripts in
one document, with the Plus Jakarta Sans webfont, the logos, and the portfolio
thumbnails inlined as data URIs. It makes no external network request.

## Design system

The stylesheet is the one from
[Custom-Web-Design](https://github.com/imageworksc/Custom-Web-Design), carried
over unchanged: the same brand tokens, the same 2px corner, the same card
recipe, the same white / tint / deep / CTA bands, and the same sticky header
and footer. Only the pieces this page needs that the web-design page had no use
for — the service chips, the brand-kit flat lay, and eight added icons — are
declared in a second `<style>` block, all prefixed `bd-`.

Two consequences worth knowing before editing:

- **Don't edit the shared stylesheet here.** Fixes belong upstream in
  Custom-Web-Design, then get carried across, or the two pages drift apart.
- `.mc-shot` (the browser-mockup screenshot on the web-design page) has been
  dropped, since nothing here draws that mockup and the data URI was 87KB.

## Content to verify before this goes live

- The stat figures — 700+ clients, 20+ awards, 28+ years — are carried over
  from the Custom Web Design page. Confirm they're current.
- The portfolio thumbnails are the web-design screenshots, re-tagged as
  branding work. Swap the eight `.work-shot--N` rules for real branding pieces
  when they're available.
- Every CTA points at the on-page `#quote` section. Repoint them at the real
  contact form on deploy.
