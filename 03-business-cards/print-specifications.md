---
title: "Anissa Russell — Business Card Print Specifications"
status: Production-Ready — Hand to Printer
prepared_by: Michael Muyot
date: 2026-05-23
version: 1.0
---

# Anissa Russell · Business Card Print Specifications
## All three directions. Hand this document to any printer and expect no follow-up questions.

---

## UNIVERSAL SPECIFICATIONS
*Applies to all three directions.*

### Dimensions

| Measurement        | Imperial          | Metric         |
|--------------------|-------------------|----------------|
| Final trim size    | 3.5" × 2"         | 88.9mm × 50.8mm |
| With bleed (all sides) | 3.75" × 2.25" | 95.25mm × 57.15mm |
| Bleed amount       | 0.125" per side   | 3.175mm per side |
| Safe zone (keep all text inside) | 3.25" × 1.75" | 82.55mm × 44.45mm |
| Safe zone margin from trim | 0.125" per side | 3.175mm per side |

> All text and the sun mark must sit within the safe zone. Background colors extend to the bleed line — never to trim only.

### File Requirements

- **Format:** PDF/X-1a or PDF/X-4 (press-ready)
- **Color mode:** CMYK only — no RGB, no spot colors unless Pantone is specified
- **Resolution:** 300 DPI minimum for all raster elements; sun mark should be vector (SVG/EPS embedded)
- **Fonts:** Embedded or outlined — never live text in the final print file
- **Layers:** Flatten before export

### Quantity and Sides
- Double-sided (front and back) for all three directions
- Recommend printing at minimum 250 cards per direction selected
- If printing all three, order in separate runs — do not mix directions in one run

---

## PAPER STOCK

### Recommended Stock
**16pt Uncoated Card Stock, Matte Finish**

Uncoated is non-negotiable for this brand. Coated or glossy stock undermines the handcrafted, tactile quality of the aesthetic. The paper should have a slight tooth — something you can feel when you hold it.

| Property       | Specification |
|----------------|--------------|
| Weight         | 16pt (preferred) or 18pt |
| Finish         | Uncoated matte |
| Laminate       | None (preferred) or soft-touch matte only |
| Texture        | Smooth uncoated or light linen texture acceptable |

**Direction-specific notes:**

- Direction A (Parchment): Natural white uncoated stock complements the parchment ground. Request "natural white" or "cream" base if available — it deepens the warmth of the parchment print.
- Direction B (Rose): Standard white uncoated. The rose blush ink does the warmth work.
- Direction C (Umber Deep): Standard white uncoated. The dark ground prints better on bright white stock — natural or cream base can muddy the deep umber. Request a proof.

### Press Proofing
Always request a physical press proof before the full run, especially for:
- Direction C: Umber Deep `#2E1F14` / CMYK 0, 31, 55, 82 — dark backgrounds can shift significantly between monitor and print
- Gold Sun `#C8922A` / CMYK 0, 27, 79, 22 — gold tones are notoriously variable; verify the warmth is preserved and it has not gone orange or flat

Pantone fallback for Gold Sun if CMYK match is unsatisfactory: **Pantone 7509 C** (uncoated)

---

## TYPOGRAPHY — EXACT SPECIFICATIONS

### Typefaces Required
All fonts must be licensed and installed before building the print file.
- Cinzel 500 — Google Fonts (free, commercial use permitted)
- Cormorant Garamond Italic 300 — Google Fonts (free, commercial use permitted)
- Cormorant Garamond Regular 400 — Google Fonts (free, commercial use permitted)
- Jost Light 300 — Google Fonts (free, commercial use permitted)

### Size and Style Per Element

| Element                  | Font                         | Size  | Tracking    | Leading   |
|--------------------------|------------------------------|-------|-------------|-----------|
| Name (front)             | Cinzel 500                   | 13pt  | 80 (0.08em) | 16pt      |
| Name (back)              | Cinzel 500                   | 10pt  | 60 (0.06em) | 13pt      |
| Tagline                  | Cormorant Garamond Italic 300| 8.5pt | 40 (0.04em) | 13pt      |
| Section label / location | Cormorant Garamond Italic 300| 7.5pt | 40 (0.04em) | 11pt      |
| Credentials line         | Cormorant Garamond Regular 400| 7.5pt | 20 (0.02em)| 11pt      |
| License number           | Cormorant Garamond Regular 400| 7pt  | 20 (0.02em) | 10pt      |
| Contact info             | Jost Light 300               | 7pt   | 60 (0.06em) | 11pt      |
| Separator dots / pipes   | Jost Light 300               | 7pt   | 40          | —         |

> Tracking values listed in Adobe units (1/1000 em). Convert as needed for your layout application.

---

## DIRECTION A — PARCHMENT ELEGANCE

### Identity
**Mood:** Quiet authority. Timeless. Works across all client archetypes. Does not close doors.

### Color Specifications

| Element          | Color Name   | Hex       | CMYK            |
|------------------|--------------|-----------|-----------------|
| Background       | Parchment    | `#F5EDD8` | 0, 3, 12, 4     |
| Sun mark         | Gold Sun     | `#C8922A` | 0, 27, 79, 22   |
| Name             | Umber Deep   | `#2E1F14` | 0, 31, 55, 82   |
| Tagline          | Bark         | `#8C7355` | 0, 17, 40, 45   |
| Credentials      | Umber Deep   | `#2E1F14` | 0, 31, 55, 82   |
| Contact          | Bark         | `#8C7355` | 0, 17, 40, 45   |
| Separators       | Bark         | `#8C7355` | 0, 17, 40, 45   |

### Layout — Front

```
┌─────────────────────────────────────────┐
│  [safe zone begins 0.125" from trim]    │
│                                         │
│            ☀ [Sun mark]                 │
│          diameter: 0.55"                │
│          centered horizontally          │
│          positioned upper-center,       │
│          top of mark at 0.3" from top   │
│                                         │
│         ANISSA RUSSELL                  │
│    [Cinzel 500 · 13pt · centered]       │
│                                         │
│  Licensed Massage Therapist             │
│     · Reiki Master Teacher              │
│  [Cormorant Garamond Reg 400 · 7.5pt]  │
│                                         │
│  Therapeutic Massage & Energy Work      │
│  [Cormorant Garamond Italic 300 · 8.5pt]│
│                                         │
│  843-283-8228 · evrgr8el@gmail.com      │
│       [Jost Light 300 · 7pt]            │
│                                         │
│  [safe zone ends 0.125" from trim]      │
└─────────────────────────────────────────┘
```

**Horizontal alignment:** All elements centered
**Vertical distribution:** Sun mark anchors top third; text stacks in bottom two-thirds with even optical spacing

### Layout — Back

```
┌─────────────────────────────────────────┐
│  Collective Wellness · Summerville, SC  │
│  [Cormorant Garamond Italic 300 · 7.5pt]│
│  [centered · top of safe zone]          │
│                                         │
│         ANISSA RUSSELL                  │
│    [Cinzel 500 · 10pt · centered]       │
│                                         │
│  Licensed Massage Therapist             │
│          License #942                   │
│      Reiki Master Teacher               │
│  [Cormorant Garamond Reg 400 · 7.5pt]  │
│                                         │
│  843-283-8228 · evrgr8el@gmail.com      │
│     FB: @AnissaRussellLMT               │
│       [Jost Light 300 · 7pt]            │
│                                         │
│          ☀ [Sun watermark]              │
│    [simplified 8-ray · 10% opacity      │
│     Gold Sun · positioned bottom-right  │
│     partially cropped by safe zone edge]│
└─────────────────────────────────────────┘
```

---

## DIRECTION B — ROSE WARMTH

### Identity
**Mood:** Tender presence. Softest entry. Most overtly healing. Closest to the original blush card.

### Color Specifications

| Element          | Color Name   | Hex       | CMYK            |
|------------------|--------------|-----------|-----------------|
| Background       | Rose Blush   | `#D4B5AD` | 0, 14, 18, 17   |
| Sun mark         | Gold Sun     | `#C8922A` | 0, 27, 79, 22   |
| Name             | Umber Deep   | `#2E1F14` | 0, 31, 55, 82   |
| Tagline          | Bark         | `#8C7355` | 0, 17, 40, 45   |
| Credentials      | Umber Deep   | `#2E1F14` | 0, 31, 55, 82   |
| Contact          | Bark         | `#8C7355` | 0, 17, 40, 45   |
| Separators       | Bark         | `#8C7355` | 0, 17, 40, 45   |

> Note: Rose Blush is a mid-value ground. Umber Deep text will have sufficient contrast. Verify on proof — the blush-to-bark combination on the contact line should not feel muddy.

### Layout — Front
Same structure as Direction A. All layout measurements identical. Only the background color changes.

### Layout — Back
Same structure as Direction A. All layout measurements identical.

**Direction B variation note:** The sun mark on the rose ground reads slightly warmer and less stark than on parchment. No layout adjustment needed — the color does the work.

---

## DIRECTION C — DEEP UMBER

### Identity
**Mood:** Grounded authority. Most striking. Strongest premium signal. Best for attracting the premium-tier archetype. The gold on dark says: I know exactly who I am.

### Color Specifications

| Element          | Color Name   | Hex       | CMYK            |
|------------------|--------------|-----------|-----------------|
| Background       | Umber Deep   | `#2E1F14` | 0, 31, 55, 82   |
| Sun mark         | Gold Sun     | `#C8922A` | 0, 27, 79, 22   |
| Name             | Parchment    | `#F5EDD8` | 0, 3, 12, 4     |
| Tagline          | Gold Pale    | `#E8C97A` | 0, 13, 53, 9    |
| Credentials      | Rose Blush   | `#D4B5AD` | 0, 14, 18, 17   |
| Contact          | Bark         | `#8C7355` | 0, 17, 40, 45   |
| Separators       | Bark         | `#8C7355` | 0, 17, 40, 45   |

> This is the only direction where the full color hierarchy plays out. Name in parchment. Tagline in gold pale. Credentials in rose blush. Contact in bark. The layering creates depth without requiring anything beyond type and the mark.

> ⚠️ PROOF REQUIRED: Umber Deep at CMYK 0, 31, 55, 82 can shift significantly on press. The target is a warm, near-black dark chocolate — not a flat brown and not a neutral black. Request a physical proof and compare against the digital reference before approving a full run.

### Layout — Front
Same structure as Direction A and B. Layout measurements identical.

**Direction C exception — sun mark treatment:**
The full sun mark on the dark ground is the strongest version of the mark across all three directions. Do not reduce the mark size for Direction C. If anything, it can be sized slightly larger (up to 0.65" diameter) because the dark ground gives it room to breathe without crowding the text.

### Layout — Back
Same structure as Directions A and B.

**Direction C back — watermark treatment:**
The simplified 8-ray sun watermark on the back, at 10–15% opacity of Gold Sun, is more visible on the dark ground than on the light grounds. Calibrate opacity so it reads as texture, not as a competing element. 10% is the starting point — adjust on proof.

---

## SUN MARK TECHNICAL SPECIFICATIONS

### Primary Mark (Full Sun — Front of All Directions)
- Type: SVG vector, embedded in print file
- Diameter: 0.55" (13.97mm) standard · 0.65" (16.51mm) maximum for Direction C
- Center position: horizontally centered; top of mark sits 0.30"–0.35" from top trim line
- Ray count: all rays, evenly spaced
- Stroke weight: rays at approximately 0.012" (0.3mm) at this size — verify visually, not mathematically
- Fill: Gold Sun `#C8922A` / CMYK 0, 27, 79, 22

### Simplified Mark (8-Ray — Back Watermark)
- Type: SVG vector
- Diameter: 0.70"–0.80" (17.78mm–20.32mm) — larger than front mark because it is a background element
- Position: bottom-right corner, partially behind safe zone edge (intentionally cropped)
- Ray count: 8, evenly spaced
- Opacity: 10% on light grounds (Direction A, B) · 12–15% on dark ground (Direction C)
- Fill: Gold Sun `#C8922A` at specified opacity

---

## PRINTER CHECKLIST
*Verify before sending to press.*

- [ ] File is CMYK, not RGB
- [ ] Resolution is 300 DPI minimum for all raster elements
- [ ] Sun mark is vector, not rasterized
- [ ] All fonts are embedded or outlined
- [ ] Bleed extends 0.125" beyond trim on all sides
- [ ] All text sits within the 0.125" safe zone margin
- [ ] Background color extends to bleed line, not trim line
- [ ] Physical proof requested before full run
- [ ] Proof compared against CMYK reference values above, not screen
- [ ] Paper specified as 16pt uncoated matte
- [ ] For Direction C: Umber Deep verified on proof before approving

---

## VENDOR NOTES

If using an online printer (MOO, Canva Print, Vistaprint Business, Overnight Prints):
- MOO is the preferred vendor for this quality level. Their "Luxe" uncoated card stock is close to spec. Request uncoated matte.
- Vistaprint's "Premium" uncoated is acceptable for a first run if budget is a constraint — verify CMYK profile support before uploading.
- Do not use any vendor that does not support custom CMYK file uploads.

If using a local print shop (Charleston/Summerville area):
- Request an ICC profile for their press before building the file, or ask them to soft-proof the PDF on their monitor against your color spec.
- Bring this spec sheet to the conversation.

---

*Anissa Russell Business Card Print Specifications // v1.0 // Production-Ready 2026-05-23 // Prepared by Michael Muyot*
