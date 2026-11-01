# Contributing to digitalplay Writing

Thanks for wanting to help. This is a small, friendly project and every tool is free.

## Suggest a tool

Open an issue on the hub repo using the **Suggest a tool** form:
https://github.com/anorthernman-developer/digitalplay-work/issues/new?template=suggest-a-tool.yml

Or start a conversation in Discussions: https://github.com/anorthernman-developer/digitalplay-work/discussions

## Build a tool

Each tool is **one HTML file** in `tools/`. No build step, no frameworks, no network calls. Open it straight from your disk and it works.

A good tool here:

1. **Is playful.** Something should happen in the first ten seconds.
2. **Takes the player's own input**: their words, photos, drawings, code or rules.
3. **Has a LEARN panel** that explains the idea in plain English (en-GB), with a little history stated as facts.
4. **Has presets** saved in the browser, with JSON export and import.
5. **Works offline** and makes no network requests. No trackers, no analytics, no cookies.
6. **Is accessible**: keyboard operable, visible focus, labels on every control, WCAG 2.2 AA contrast, respects reduced motion.

Add an entry to `catalogue.json` that matches `catalogue.schema.json`, using the facet values in the hub's `taxonomy.json`.

## The rules we don't bend

- **No living artist's name or likeness** in a tool name, branding or any AI prompt that imitates a named person. Influences go in a short factual "inspired by" line, for example "the cut-up method (around 1959)".
- **No copyrighted material** without a licence: no quotes, lyrics, scores, images or fonts you don't have the right to use. Fonts must be OFL or system fonts.
- **No personal data.** Tools never collect or send anything.
- **Never commit an API key.** If a tool offers optional AI, the visitor pastes their own key and it is stored only in their browser's localStorage. Run a secret scan before you push:

  ```
  grep -rnE "AIza[0-9A-Za-z_-]{20,}|ghp_[0-9A-Za-z]{20,}|sk-[0-9A-Za-z]{20,}|xox[abp]-" .
  ```

## Licences

Code: MIT. Written content: CC BY 4.0. By contributing you agree your contribution is released under the same terms.
