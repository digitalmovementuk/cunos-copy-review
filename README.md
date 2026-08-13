# Cunos Consulting — hero, H2 and H3 review

**Open the review link we sent you.** Nothing to install, nothing to sign into.
Your edits save themselves as you type — to your own browser first, and to our
server a second later, so a closed tab or a flat battery costs nothing.

One page to read and rewrite every headline on cunos.co.uk. Built 13 August 2026.

There is also a single-file copy, `hero-h2-review.html`, that works with no
internet connection at all. It keeps edits in that one browser only, so it is the
offline fallback rather than the normal way in.

## What is in it

All four pages the site has — the homepage and the three service pages — and for
each of them, in the order they appear as you scroll:

- the small line above the big headline
- the big headline itself
- the paragraph under it
- every section heading (H2) with the small line above it
- every sub-heading (H3) beneath those

**170 boxes in all**, made up of 224 lines: 50 section headings and 59 sub-headings.

Sub-headings are here because Google's own guidance, and the Yoast checker this tool
runs, treat an H3 exactly like an H2. Leaving them out would have set a target you
could not reach from inside the tool.

Under each section heading there is a paragraph in grey. That is the first paragraph
of the section, shown so you can judge whether the heading still matches what the
section goes on to say. It is there to read, not to edit.

## Where the words came from

Read off the live site, `https://cunos.co.uk`, on 13 August 2026 — the copy as it
actually appears on screen, not a document about it.

That is less obvious than it sounds. Cunos is a React site: the file the server sends
is empty, and every word is written in by the browser a moment later. So the pages
were opened in a real browser and read from there. Anything else would have come back
blank.

Every one of the 224 lines was then traced back to the file that has to change for the
edit to survive the next time the site is rebuilt. **224 of 224 were found** — nothing
on the site is copy the source cannot account for.

| Lines | Lives in |
| -----: | -------- |
| 43 | `src/App.tsx` — the homepage and the footer |
| 52 | `src/services/SeniorFinanceSupport.tsx` |
| 64 | `src/services/CashflowForecast.tsx` |
| 65 | `src/services/ManagementReport.tsx` |

Three of them — the opening paragraph on each service page — are written across
several lines in the file. The tool says so under the box, because searching the file
for the sentence as one line will not find it.

## Why a headline is split into several boxes

Because that is how the site was written. Cunos headlines are built from parts that
fade in one after another, and each part is its own piece of text in the source. So
"Ready for clearer finance control?" arrives here as four boxes.

Above them the tool shows **reads as** — the whole heading as one sentence, updating
as you type. Edit the boxes; read the sentence.

## What it will not let you do

Press **SEO rules** in the top bar for the full table. In short, each box refuses
characters past a cap: a big headline stops at 60, a section heading at 70, a
sub-heading at 65, a small kicker line at 45, an opening paragraph at 320. A line that
is already over its cap can only be shortened, and "revert this line" always puts the
original back.

Yoast does not measure the length of a heading at all, so those numbers are ours: 60
characters is the budget Yoast gives a page title. The rules table says, per limit,
whose number it is.

**Seven boxes are over their cap today**, before anyone types anything:

- the homepage's first section heading, at 143 characters against 70
- the cashflow page's headline (90 against 60), two of its section headings and one
  sub-heading
- the management reporting page's headline (94 against 60) and one sub-heading

The two headlines are over because each one carries a second, explanatory line inside
the same heading. That is a deliberate design, not a mistake — but it is still inside
the H1, so the tool counts it. Those pages can still be marked reviewed; see below.

## The checks, and who is doing the checking

Under each page's title is a panel listing **every check Yoast runs** — all 16 search
ones and all 6 readability ones — in Yoast's own words, with Yoast's own red, amber
and green.

Nothing here re-implements a Yoast rule. The plugin's own analysis engine, Yoast SEO
28.2, is embedded in this page and actually run, on the page rebuilt with your edits,
every time you stop typing for a third of a second.

One thing to be straight about: **these pages have never been in WordPress**, so Yoast
has never seen them and there is no second opinion to compare against. Everything the
panel says is Yoast's engine applied to the words the live page serves. It is the same
engine, on the same words — but treat a borderline number as borderline.

**What stops a page being ticked off, and what doesn't.** A red blocks a review only
when the fix is *here* — in the headings. The page title, the description, the images
and the links are all shown, keep Yoast's red, and are labelled "fix in the component
file · never blocks a review". When a page will not tick off, the footer names what it
ignored, so a red image row is never mistaken for the reason.

And it is never a dead end. Every page that will not tick off offers "let me tick it
off anyway" — including the pages whose only sticking point is a headline that was
already over its cap. Taking that route is recorded in the export as
`overridden: true`, never hidden.

## Two Yoast habits that surprise people

- It counts a match when **every word of the search term turns up in the same
  sentence**, in any order. "finance director, outsourced" counts for "outsourced
  finance director".
- It throws away small words first, so **best, new, top, near** never count.

## About the search terms

This is the part to read before rewriting a hero, and it is the part where the
research is genuinely unfinished. Rather than show a tidy number, each page says what
is actually known:

| Page | Search term | What is on file |
| ---- | ----------- | --------------- |
| Homepage | — | No term has been chosen for it. The keyphrase checks are switched off and the page is judged on how it reads. |
| Senior Finance Support | outsourced finance director | 320 searches a month (May 2026). Results page read 9 August 2026 — the cleanest in the study. No measured difficulty. |
| 13-Week Cashflow Forecast | cash flow forecasting services uk | Results page read 9 August 2026, judged worth pursuing. No volume, no difficulty. |
| Monthly Management Reporting | management accounts service london | Results page read 9 August 2026, rated the strongest of the three. No volume, no difficulty. |

Three of the four pages therefore sit in a state of their own — **part-researched** —
rather than being shown as verified. The alternative was to borrow a figure from a
similar phrase: "cash flow forecast" has 3,600 searches a month on file, and it would
have been easy to put that number against "cash flow forecasting services uk". It is a
different search. Its number is not that page's number, so it is not shown.

Sources: `_seo-strategy-2026-08-09/target-keywords.json` for the terms and the results
pages, `Pitches/cunos-co-uk-seo-data.json` for the one volume figure.

## How to use it

- Click a page in the left list, or press `J` / `K` to move.
- Type straight into any box. Edits save themselves in the browser, so you can close
  the tab and come back.
- "Mark reviewed" ticks the page off and jumps to the next (`⌘ Enter`).
- When you are done — or part-way, it does not matter — press **Export edits**, then
  **Copy to clipboard** or **Download .json**, and send that back.

**Nothing you type changes cunos.co.uk.** The site is untouched until someone applies
the export and rebuilds it.

## Where your edits go

Top right of the bar there is a small badge. It is always telling you the truth
about where your work is:

| It says | What that means |
| ------- | --------------- |
| **Saved 14:32** | In your browser *and* on our server. Nothing to do. |
| **Saving…** | On its way. Takes about a second. |
| **Not saved yet — retrying** | The server did not answer. Your work is safe in this browser and it will keep trying by itself. |
| **Offline — kept in this browser** | Same, for a dropped connection. It resumes on its own. |
| **This browser only** | You opened the offline file rather than the link. Edits stay on this machine — press Export when you finish. |

Because the saving goes to us rather than to the browser alone, **the link works on
more than one device**: start on the laptop, open the same link on your phone, and
it carries on where you left off. Whichever one you typed in most recently wins.

Every version is kept, not just the latest, so a bad paste at eleven o'clock never
destroys what was there at five to.

**Treat the link like the document itself.** There is no password — anyone holding
that link can edit this review, so please do not forward it.

## What comes back out

**Export edits** produces one JSON file holding:

- every changed line, with the file it has to land in, the exact text to search for,
  and how many times that text appears on the page
- `rules` — the caps the editing was done under, and which Yoast version produced the
  numbers
- `yoast_checks` — per page: both scores, every Yoast result word for word, which of
  them are fixed elsewhere, which boxes are over their cap, and `overridden: true`
  where a page was ticked off past a failing check

That is enough for whoever applies the edits to check the numbers against the plugin
rather than take them on trust.

## Rebuilding it

Three files sit beside this one and run in this order:

1. `node render_cunos.mjs` — opens the four live pages in a browser and caches them in
   `html-cache/`. Delete that folder first to force a fresh read. Playwright is
   borrowed from `Websites/Azura Living Bali/node_modules`, which is the only checkout
   in the repo that carries it.
2. `python3 extract_cunos.py` — reads the cached pages, finds every heading, traces
   each line back to its source file, and writes `cunos-headings.json`.
3. `python3 build_cunos_review.py` — writes `hero-h2-review.html`.

Then `node qa_review_tool.mjs` opens the built tool in a browser and checks it works —
that the Yoast engine loaded, that typing registers, that nothing runs off the edge of
a phone screen. It writes screenshots to `.qa/`. A clean read of the source proves
none of that.

`python3 build-html-twins.py` regenerates `README.html` from this file.

`./publish.sh` copies the built tool and this guide into `site/` and pushes them to
the `cunos-copy-review` repository, which is what GitHub Pages serves. The autosave
endpoint is a separate deploy: `cunos-review.php` lives with the other endpoint
files in `Sales/SEO Strategies/DM UK Own Site .../leads-endpoint-source/` and goes
up as part of that folder's zip. Its store is `pplus-store/cunos-review/` on the
server, above the web root, one file for the latest state and one for the history.
The reviewer keys are in `_review-keys.txt` here, which is deliberately not in any
repository — only the SHA-256 of each key is on the server.

The Yoast engine itself is **not** in this folder. It lives once, at
`Operations/yoast-live/`, and is shared with the DM UK, DM NZ, Husband Retail and CEx
review tools.

## One thing that changed in the shared engine

Building this tool turned up a real bug in that shared engine, and it is fixed there
rather than worked around here.

A page with no search term set — this site's homepage — was being given an SEO score
of **−676**. Yoast marks a check it cannot run with a placeholder score rather than by
leaving it out (−999 for "no keyphrase set", −50 for density), and Yoast's own
averaging then treats those placeholders as scores. In WordPress you never see it,
because Yoast refuses to show a score at all until a keyphrase is entered.

The engine now does the same: no keyphrase, no SEO score, and the chip says
"SEO not scored — no keyphrase set" in words. Readability is unaffected, and so is any
page that has a keyphrase — none of the other four tools has a page without one, so
none of their numbers move.
