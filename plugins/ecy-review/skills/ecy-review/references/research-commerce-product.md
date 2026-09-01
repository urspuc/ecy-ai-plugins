# Research, commerce, product and manual review

Choose the relevant section. Do not run every section by default.

## Research and competitor analysis

Identify the 3–5 claims most capable of changing the recommendation. For each, check:

- exact wording and scope: market, country, channel, product, population, and time range;
- source existence, publication date, source quality, and whether it is first-party, independent reporting, marketing, or user opinion;
- direct support: the source must prove the claim, not merely discuss the same topic;
- currentness and whether newer information could reverse the claim;
- fact, inference, assumption, estimate, or opinion;
- contradictory evidence and how the artifact handles it;
- competitor inclusion criteria and missing substitutes, regional brands, low-price alternatives, or non-product alternatives;
- selection, survivorship, platform, and small-sample bias;
- whether each recommendation follows from the evidence rather than from a preselected conclusion.

For Deep review, produce a claim ledger when it improves clarity:

| Claim | Type | Source | Direct support? | Current? | Contradictory evidence / gap | Verdict |
| --- | --- | --- | --- | --- | --- | --- |

Do not invent a source. If live source checking was not performed, mark the factual claim `UNABLE TO VERIFY` even when it sounds plausible.

## Ecommerce, Amazon and listings

Use the authoritative specification and policy for the exact SKU, version, color, region, and sales channel. Check:

- model, layout, color, switch or component variant;
- dimensions, weight, materials, battery, connectivity, interface, and included accessories;
- operating-system, connector, firmware, accessory, and layout compatibility conditions;
- consistency among title, bullets, description, A+, images, FAQ, and official specification;
- whether a feature claim is documented product behavior or an inference;
- absolute or hard-to-prove claims such as “best”, “perfect”, “guaranteed”, “never”, and “all devices”;
- warranty, price, promotion, shipping, gifts, inventory, and regional policy authorization;
- terminology used by the target market rather than literal translation;
- missing facts likely to cause returns, support tickets, or negative reviews.

Treat old models and nearby colorways as separate products unless the evidence explicitly establishes shared specifications.

## Product specifications, manuals and FAQs

Use confirmed firmware behavior, QA test cases, product specifications, and real-device evidence. Check every operational statement for:

- key combination, press duration, action order, and current mode;
- LED color, blinking or steady state, trigger, duration, and end condition;
- wired, Bluetooth, 2.4G, charging, battery, pairing, re-pairing, and recovery behavior;
- prerequisites, first-use path, exceptions, and failure recovery;
- OS-specific and hardware-version-specific paths;
- hardware names, functional terms, icons, diagrams, key maps, and cross-page consistency;
- whether a new user can complete the task using only the published steps;
- authorized power, charger, warning, warranty, and safety wording;
- mismatch between diagrams, tables, screenshots, and prose.

Do not fill missing product behavior from general technical knowledge. Mark it `UNABLE TO VERIFY` and name the exact firmware, QA, product owner, or real-device evidence needed.

For Deep manual review, end with the highest-risk real-device test paths. A successful language review is not evidence that the instructions work on the device.

## Human judgment boundary

People approve the final product facts, positioning, warranty and pricing policy, risk tolerance, competitor importance, and market-entry decision.
