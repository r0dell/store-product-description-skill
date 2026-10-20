---
name: store-product-description
description: Writes conversion-focused product descriptions for Shopify and other online stores, in the store's brand voice, with scannable benefits, specs, and SEO-friendly wording, output as clean HTML or plain text. Use when the user asks to write, rewrite or improve a product description, product page copy, or bulk descriptions from a list or CSV.
---

# Product Description Writer

## Inputs
Use what the user provides; ask once (in a single message) only for what is truly missing:
- Product name, type, price range (optional)
- Facts: materials, dimensions, sizes, colours, care, what's included, origin
- Target customer and main use case
- Brand voice profile (if one exists in the conversation or project, follow it strictly; otherwise use a warm, clear, confident default)
- Output format: Shopify "Body (HTML)" (default) or plain text
- Main keyword (optional)

Never invent facts. If a fact is missing (e.g. material), leave it out or mark it as `[CONFIRM: ...]` for the user.

## Structure (default)
1. **Hook** – 1–2 sentences: the outcome or feeling for the customer, not the feature.
2. **Benefits** – 3–5 bullets. Each: benefit first, then the feature that proves it ("Stays warm for 12 hours – double-wall vacuum steel").
3. **Details** – short paragraph: who it's for, how to use it, what makes it different.
4. **Specs** – compact list: size, material, weight, care, what's in the box.
5. **Reassurance** – one line on shipping/returns/guarantee ONLY if the user gave the policy.

Length: 120–220 words unless the user asks otherwise. Mobile shoppers scan: short paragraphs, no walls of text.

## SEO rules
- Use the main keyword naturally in the first sentence and once more in the body. No keyword stuffing.
- Use words customers actually search and say (e.g. "linen tablecloth" rather than "textile table covering").
- Do not copy manufacturer text verbatim (duplicate content); always rewrite.

## HTML output rules (Shopify Body HTML)
- Allowed tags: `<p>`, `<ul>`, `<li>`, `<strong>`, `<h3>`, `<br>`. No inline styles, no `<h1>` (the theme uses the product title as H1), no scripts.
- Return the HTML in one code block so it can be pasted into the HTML view of the editor.

## Claims and compliance
- No health/medical claims, no "best/#1" without proof, no fake scarcity ("only 2 left") unless true, no fake reviews.
- For cosmetics, supplements, children's products or electrical items: add `[CHECK: regulatory wording]` where a claim might need verification.

## Bulk mode
If the user gives several products (list or CSV rows): write one description per product, keep the structure identical, vary the hooks so pages don't read as duplicates, and return a table or CSV with columns `Handle, Body (HTML)` when they came from a CSV.

## Example
Input: "Handmade ceramic mug, 350 ml, stoneware, dishwasher safe, speckled glaze, made in Portugal. For slow-morning coffee lovers."

Output (HTML):
```html
<p>Make your first coffee of the day a small ritual. This handmade stoneware mug feels solid in your hands and keeps every sip just a little more special.</p>
<ul>
<li><strong>Generous 350 ml</strong> – room for a proper flat white or a big mug of tea</li>
<li><strong>Every piece is unique</strong> – hand-thrown, with a speckled glaze that varies slightly</li>
<li><strong>Everyday tough</strong> – durable stoneware that goes straight into the dishwasher</li>
</ul>
<p>Made by a small workshop in Portugal for people who like their mornings slow and their objects honest.</p>
<h3>Details</h3>
<ul>
<li>Capacity: 350 ml</li>
<li>Material: stoneware, speckled glaze</li>
<li>Care: dishwasher safe</li>
</ul>
```
