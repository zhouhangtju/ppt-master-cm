---
description: Verify layout density and eliminate top-heavy / bottom-empty pages before export
---

# Verify Layout Density Workflow

> Standalone post-generation check. Run after SVG generation and before post-processing when the deck follows a China Mobile-style dense reporting language or when a generated deck visually feels too sparse.

This workflow focuses on structure and density, not SVG syntax correctness. It complements `svg_quality_checker.py`.

## When to Run

- the deck is information-dense and should not look sparse
- the user asked for China Mobile style, operator internal reporting style, or a strong consulting-style structure
- generated pages feel top-heavy, bottom-empty, or visually weak despite being technically valid

## What to Check

For each content page:

1. does the content area feel at least roughly 80% used?
2. is the page top-heavy with a large blank lower half?
3. are there visible modules filling the page rhythmically?
4. does the page end with a visible judgment, takeaway, or action line?
5. is the page using structure, not only shrinking text or widening whitespace?

## Common Failure Modes

- large title plus a few weak cards
- chart or screenshot with no conclusion
- content squeezed into the upper half
- overuse of whitespace to avoid overflow
- application pages reduced to broad labels
- progress pages with no milestone or action structure

## Correction Order

When a page fails, adjust in this order:

1. increase content density with more evidence or support modules
2. change the pattern instead of shrinking type first
3. redistribute the layout regions vertically
4. increase spacing or font size only if the page is structurally sound but visually too empty
5. add auxiliary structural elements such as tags, status chips, or judgment bars

## Never Do

- never invent facts to fill space
- never add meaningless decoration only to occupy area
- never weaken a mature reference style into generic blue-white cards
- never rely only on shrinking type to solve structure problems

## Receipt Format

Output one line per checked page:

```text
verify-layout-density: P05 | result=pass | note=dense structure holds
verify-layout-density: P06 | result=fix-needed | reason=top-heavy, no bottom judgment strip
```

## After Corrections

If any page changed:

1. rerun `svg_quality_checker.py`
2. rerender and visually recheck the touched pages
3. continue to post-processing only after the sparse-layout issues are resolved
