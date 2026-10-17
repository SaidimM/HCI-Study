---
type: teardown
medium: print    # print | web | app
source: "{{publication or URL}}"
date: {{date}}
tags: [teardown, visual-design, layout, color]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
TEARDOWN · {{MEDIUM}}
</p>

# {{title}}

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">FIRST IMPRESSION · 3 SECONDS</p>
    <p>What did the eye hit first, second, third? What did you *feel*?</p>
  </div>
  <div style="flex: 0.8; max-width: 260px; flex-shrink: 0;">
    <img src="assets/{{image}}" alt="{{title}}" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Argumentative Caption:</strong> one sentence arguing what this layout achieves.
    </p>
  </div>
</div>

---

## Structure
```
┌──────────────────────────────────────────┐
│ grid · margins · gutters · hierarchy     │
└──────────────────────────────────────────┘
```
- **Hierarchy levers:** size / weight / color / position / space
- **Color:** palette, role of each color, contrast
- **Whitespace:** where, how much, why

## Editor's intention
Why this arrangement? What story, mood, or brand does it serve?

## What breaks the rules, and why it works

## Steal this
Reusable pattern → [[concept]]

## Recreation
Link to Figma/HTML attempt.

## My thoughts
