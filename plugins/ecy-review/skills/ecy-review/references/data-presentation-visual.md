# Data, presentation and visual review

Use the relevant section and inspect the real file or render whenever available.

## Spreadsheet, CSV, Excel and data conclusions

Do not validate numbers by visual plausibility. Recalculate whenever tools and source data permit.

Establish the source file, sheet, row count, field definitions, date range, filters, aggregation level, units, currency, tax treatment, and refresh time. Then check:

- missing values, duplicates, blanks, zeroes, negatives, refunds, cancellations, and outliers;
- subtotal, grand total, percentage, average, weighted average, and growth calculations;
- numerator and denominator alignment across time, region, channel, product, and population;
- formula ranges, omitted added rows, hard-coded values, broken references, and filtered-versus-unfiltered totals;
- currency, exchange rate, tax, unit, date format, and timezone consistency;
- whether source rows, summaries, charts, and narrative conclusions reconcile;
- small samples, abnormal periods, correlation, and unsupported extrapolation.

For important metrics, independently reconcile:

| Metric | Reported | Independently calculated | Match? | Difference / reason | Verification needed |
| --- | --- | --- | --- | --- | --- |

When a fast sanity check is appropriate, inspect ten representative rows: high, low, blank/zero/negative or unusual, different dates/channels, and random rows. If the file cannot be calculated, do not say the numbers are verified.

## PPT, documents and reports

Review both content and production.

Content and storyline:

- Does the artifact answer the original question and make the requested decision or action clear?
- Is each slide or section organized around one main message?
- Is the heading a supported conclusion or merely a topic label?
- Does evidence support the conclusion and disclose limitations or uncertainty?
- Are there redundant pages, unsupported jumps, or missing decision steps?
- Do charts, source notes, units, time ranges, numbers, and body text agree?

Production:

- font, size, color, alignment, spacing, page number, and layout consistency;
- overflow, crop, stretched or low-resolution images, placeholders, and unreadable text;
- editable-chart requirements and whether charts remain editable;
- whether exported PDF or image output preserves the intended layout.

If only extracted text is visible, production claims must be `UNABLE TO VERIFY`. Render or inspect the actual slides/pages before claiming production readiness.

## Images and visual design

Check against the brief, then inspect local regions systematically:

- people, products, scene, count, pose, proportions, composition, colors, aspect ratio, and prohibited elements;
- anatomy, hands, fingers, joints, object count, product geometry, key layout, perspective, shadow, reflection, overlap, repetition, edge artifacts, and impossible physical relationships;
- visible text, spelling, numbers, logo accuracy, brand colors, and typography;
- pixel dimensions, crop, safe zone, transparency or background, print/screen use, and whether an editable or layered source is required.

Every visual issue must name the exact region, such as “lower-right package label”. If the region is too small or the brand master is unavailable, use `UNABLE TO VERIFY`.

## Human judgment boundary

People decide metric definitions, treatment of outliers, acceptable sample size, story and persuasion strategy, brand fit, aesthetic quality, and final production approval.
