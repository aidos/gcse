# Revision map brief

Attach this file and `revision-map-base.html` to a new chat, along with the school's key sheets for the subject. Then say something like: "Here's the brief and template. Please make the revision map for these sheets."

## Who it's for

My 15-year-old is autistic and capable. They're doing GCSEs (IGCSE for English Language). The school gives out one "key sheet" per module. Each sheet is a dense list of terms, concepts and tips. Taken together, the sheets make my teen feel they don't understand a subject they actually handle fine. The goal is to show that the subject is smaller and more connected than the sheets make it look.

## What to make

One interactive page per subject. Publish it as a claude.ai artifact, built from `revision-map-base.html`. Only edit the `DATA` section. The engine and CSS are shared, so only change them if a subject truly needs something new, and then add to them rather than rewriting.

Pages already made, as reference for tone and shape:
- Maths, a tree of five big ideas: https://claude.ai/artifact/BUNuPAMKKHUGqPVjgX2QTf
- An Inspector Calls, a chain in questioning order, linked to Eva: https://claude.ai/artifact/KxFcmFYcXNAYU3ukJHXTAa
- English Language, two papers, each with Read and Write: https://claude.ai/artifact/Huhndtot6Sn6ehCE31e8LB

## Process

1. **Read every sheet first and find the subject's natural shape.** This is the most important step, so think about it rather than using a default tree. Good shapes so far came from the subject itself: the order the Inspector questions people, and the exam's own two-paper split. Pick one of the template's three nav shapes:
   - `tree`: 4–6 big ideas.
   - `chain`: a real sequence, with an optional hub node that everything links to.
   - `groups`: two or three groups, each with 2–3 nodes.
   Cross-cutting views go in `extras`, for example themes, essay method, skills, or "spot it, use it".
2. **Merge duplicates across sheets.** Sheets often repeat each other. Sometimes a whole section is copied from another module by mistake. Say how much was repeated, because "this is the same six rules on four sheets" is part of the point.
3. **Give every section the same layout.** Quick facts first, then tickable rows, then one "Remember" line. Predictability matters more than variety.
4. **Write the content using the rules below.**
5. **Check facts and quotes** (see "Checking" below).
6. **Build, render-check and publish.** Change `storageKey` for each page. Check the page on desktop and mobile widths.
7. **Reply to me** using the format at the end of this brief.

## Content rules

- **Plain language.** Give one short rule per item and one small example. Write the rule as if explaining it to a friend.
- **Put jargon in the "Also called" line (`aka`), not in titles.** Every page ends with a "Same thing, different names" section that maps the sheet's terms to plain words, for example "index = power = exponent" or "WHAT→HOW→WHY = Claim→Evidence→Explore→Connect". These pairings help a lot, so look for them.
- **Ticks go on skills and quotes, not facts.** The tick labels are "I can do this", "I know this", "I can spot this", "I can use this" and so on. Ticks fill the dots on that branch's node.
- **Use numbered steps only for real sequences.** Story stages, essay timings and article structure count. A list of techniques does not.
- **Original examples are fine but must be mine, not the school's.** Keep them short and on the sheet's own topics where possible (plastic, Gothic). Tell the parent which examples are original.
- **Quotes stay short and exact.** Never invent or "tidy" a quote.
- **Stick to what the sheets cover.** If the sheets stop partway through a text, like Act 2 of a play, mark the gap on the page ("not on the sheets yet") and don't spoil later parts.
- **Typography:** use curly apostrophes and quotes (’ “ ”) in visible text, and sentence case. No ALL-CAPS labels.

## Checking

- **Search the web to verify quotes from set texts before using them.** Earlier sheets contained invented quotes and the wrong author name. If a sheet's quote can't be found in the real text, leave it off the page and tell me.
- **Flag sheet errors in the chat, not on the page.** The page should be calm and correct. I decide whether to raise it with the school.
- **Check any maths or science worked example by calculating it.**

## Design (already built into the template)

- Atkinson Hyperlegible, a font designed for legibility. Calm pale sage background, one colour per section (`c1`–`c6`), and `tool` for extras. Light and dark mode.
- Only one section is shown at a time, with a "Show everything" toggle. Printing shows everything.
- No decorative motion. Respects reduced-motion settings. Visible keyboard focus.
- Ticks are saved in the browser's local storage.

## Template gotchas

- In `chain`, the hub id must not also be in the row of nodes.
- `rows` with `style:"maths"` puts the working in a monospace box. Build the explanation with `s()`, `a()` and `nt()`, and use `f(a,b)` for stacked fractions.
- One-off visuals, like the story-mountain SVG, go in an `html` block. Use CSS variables for colours so dark mode works.
- `table` with `srcCol` puts a small grey note under the first cell. Pass the note as an extra item at the end of each row.

## How to reply to me

Keep it short and in prose:
- **The shape you chose and why.** One or two sentences.
- **What each section contains.** Briefly.
- **Problems with the sheets:** duplicates, errors and unverifiable quotes, with sources for any corrections.
- **Anything you invented,** like example stories or lines.
- **At most one question,** and only if it's needed.
