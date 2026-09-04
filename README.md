# langreel-site

Deploy target for **https://langreel.com** — GitHub Pages serves this repository's root.

**Do not edit these files here.** They are generated. The source lives in the LangReel
app repository under `website/langreel/` (one copy of each page, with `data-i18n` keys)
and `website/i18n/<lang>.json` (the text for each of the eight locales):

```bash
node scripts/build-langreel-site.mjs --cname   # → dist/langreel-site/
```

Then copy `dist/langreel-site/` over this repository's root and push.

`--cname` writes the `CNAME` file that points Pages at `langreel.com`. It is omitted while
the domain has no DNS records: with `CNAME` present, Pages redirects
`engdojo.github.io/langreel-site/` to a host that does not resolve, and the site becomes
unreachable from anywhere. Add it once `langreel.com` resolves.
