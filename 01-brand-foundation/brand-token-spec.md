---
title: "Anissa Russell — Brand Token Specification"
status: LOCKED — Foundation Layer for All Deliverables
prepared_by: Michael Muyot
date: 2026-05-23
version: 1.0
---

# Anissa Russell · Brand Token Specification
## The foundation layer. Every deliverable — HTML tools, print specs, copy docs — inherits from here.

---

## 1. Color Tokens — Named to Semantic Mapping

### Named Palette (Warm Alchemist)

| Token Name        | Hex       | RGB              |
|-------------------|-----------|------------------|
| `--color-parchment`  | `#F5EDD8` | 245, 237, 216    |
| `--color-linen`      | `#EDE3CC` | 237, 227, 204    |
| `--color-rose-blush` | `#D4B5AD` | 212, 181, 173    |
| `--color-rose-pale`  | `#EDD8CF` | 237, 216, 207    |
| `--color-gold-sun`   | `#C8922A` | 200, 146, 42     |
| `--color-gold-pale`  | `#E8C97A` | 232, 201, 122    |
| `--color-sage`       | `#7A8C72` | 122, 140, 114    |
| `--color-bark`       | `#8C7355` | 140, 115, 85     |
| `--color-umber-deep` | `#2E1F14` | 46, 31, 20       |

> Umber Deep `#2E1F14` locked 2026-05-23. Previous iteration `#3D2B1F` is deprecated. Do not use.

### Semantic Role Mapping

These are the roles each color plays across all deliverables. Use role names in CSS — not raw hex — so every file stays consistent.

```css
:root {
  /* Surfaces */
  --surface-primary:    #F5EDD8;  /* parchment — default background */
  --surface-secondary:  #EDE3CC;  /* linen — panels, cards, inset areas */
  --surface-warm:       #EDD8CF;  /* rose pale — alternate soft ground */
  --surface-dark:       #2E1F14;  /* umber deep — Direction C ground, strong contrast */

  /* Accent */
  --accent-primary:     #C8922A;  /* gold sun — the mark, primary CTA, active states */
  --accent-warm:        #E8C97A;  /* gold pale — hover states, highlights, warmth layer */
  --accent-blush:       #D4B5AD;  /* rose blush — secondary warmth, feminine register */
  --accent-sage:        #7A8C72;  /* sage — grounding, nature register, tertiary accent */

  /* Text */
  --text-primary:       #2E1F14;  /* umber deep — all body text on light grounds */
  --text-secondary:     #8C7355;  /* bark — supporting text, labels, captions */
  --text-on-dark:       #F5EDD8;  /* parchment — all text on umber deep ground */
  --text-accent-dark:   #E8C97A;  /* gold pale — subheads, taglines on dark ground */
  --text-credential:    #D4B5AD;  /* rose blush — credentials, secondary info on dark */

  /* Borders */
  --border-light:       #EDE3CC;  /* linen — dividers on parchment ground */
  --border-mid:         #8C7355;  /* bark — stronger dividers, form field edges */
  --border-gold:        #C8922A;  /* gold sun — active/focus state borders */
}
```

### CMYK Conversions (Print Use)

| Color        | Hex       | C    | M    | Y    | K    | Notes |
|--------------|-----------|------|------|------|------|-------|
| Parchment    | `#F5EDD8` | 0    | 3    | 12   | 4    | Request uncoated paper match |
| Linen        | `#EDE3CC` | 0    | 5    | 17   | 7    | |
| Rose Blush   | `#D4B5AD` | 0    | 14   | 18   | 17   | |
| Rose Pale    | `#EDD8CF` | 0    | 8    | 13   | 7    | |
| Gold Sun     | `#C8922A` | 0    | 27   | 79   | 22   | Specify Pantone 7509 C as fallback |
| Gold Pale    | `#E8C97A` | 0    | 13   | 53   | 9    | |
| Sage         | `#7A8C72` | 13   | 0    | 19   | 45   | |
| Bark         | `#8C7355` | 0    | 17   | 40   | 45   | |
| Umber Deep   | `#2E1F14` | 0    | 31   | 55   | 82   | Darkest — verify on press proof |

> Printer note: All cards should be printed on uncoated stock (see Step 3 spec). CMYK values above are for offset and digital offset. Inkjet proofs will vary — always request a physical proof before full run.

---

## 2. Typography Tokens

### Typeface Stack

| Token               | Family                    | Weight | Style   | Use |
|---------------------|---------------------------|--------|---------|-----|
| `--font-display`    | Cinzel                    | 500    | Normal  | Name, primary display headers |
| `--font-tagline`    | Cormorant Garamond        | 300    | Italic  | Taglines, poetry-level copy, secondary headers |
| `--font-body`       | Cormorant Garamond        | 400    | Normal  | Credentials, card body, supporting text |
| `--font-utility`    | Jost                      | 300    | Normal  | Contact info, labels, small utility text |

Google Fonts import string (for HTML tools):
```
https://fonts.googleapis.com/css2?family=Cinzel:wght@500&family=Cormorant+Garamond:ital,wght@0,400;1,300&family=Jost:wght@300&display=swap
```

> Zero-dependency HTML tools: embed this import at the top of the `<style>` block. Falls back to Georgia / serif if fonts fail to load — acceptable degradation.

### Size Scale by Context

| Context              | Font Token       | Size     | Line Height | Letter Spacing | Color Token |
|----------------------|------------------|----------|-------------|----------------|-------------|
| Primary name (card)  | `--font-display` | 16–18px  | 1.2         | 0.08em         | `--text-primary` or `--text-on-dark` |
| Section header       | `--font-display` | 13–14px  | 1.3         | 0.06em         | `--text-primary` |
| Tagline              | `--font-tagline` | 11–13px  | 1.5         | 0.04em         | `--text-secondary` or `--text-accent-dark` |
| Body copy            | `--font-body`    | 15–16px  | 1.75        | 0.01em         | `--text-primary` |
| Credentials (card)   | `--font-body`    | 9–10px   | 1.4         | 0.02em         | `--text-secondary` or `--text-credential` |
| Contact / utility    | `--font-utility` | 9–10px   | 1.4         | 0.06em         | `--text-secondary` |
| Form labels          | `--font-utility` | 13px     | 1.5         | 0.04em         | `--text-primary` |
| Button text          | `--font-utility` | 13–14px  | 1           | 0.08em         | `--accent-primary` or `--text-on-dark` |
| Small labels/chips   | `--font-utility` | 10–11px  | 1           | 0.06em         | `--text-secondary` |

---

## 3. Spacing Scale

Used for padding, margin, and gap in HTML tools. Consistent scale prevents visual clutter.

| Token         | Value  | Use |
|---------------|--------|-----|
| `--space-xs`  | 4px    | Icon gaps, tight inline spacing |
| `--space-sm`  | 8px    | Button padding (vertical), field internal gap |
| `--space-md`  | 16px   | Standard component padding |
| `--space-lg`  | 24px   | Section spacing, card padding |
| `--space-xl`  | 40px   | Major section breaks |
| `--space-2xl` | 64px   | Page-level breathing room |

---

## 4. Component States (HTML Tools)

### Interactive Elements

All interactive components in the HTML tools (quiz, intake form) follow this state system.

#### Checkbox / Option Card
| State    | Background         | Border                  | Text                  | Notes |
|----------|-------------------|-------------------------|-----------------------|-------|
| Default  | `--surface-secondary` | `--border-light`     | `--text-primary`      | |
| Hover    | `--surface-warm`   | `--border-mid`          | `--text-primary`      | Subtle warm lift |
| Selected | `--surface-warm`   | `--accent-primary` (2px)| `--text-primary`      | Gold border signals selection |
| Focused  | `--surface-secondary` | `--border-gold` (2px)| `--text-primary`      | Keyboard nav |
| Disabled | `--surface-primary`| `--border-light` (dashed)| `--text-secondary`   | Muted, not interactive |

#### Button (Primary — Generate / Send)
| State    | Background       | Border              | Text              | Notes |
|----------|-----------------|---------------------|-------------------|-------|
| Default  | `--accent-primary` | none             | `--text-on-dark`  | Gold ground |
| Hover    | `--accent-warm`  | none                | `--text-primary`  | Lightens to gold pale |
| Active   | `--color-gold-sun` (90% opacity) | none | `--text-on-dark` | Slight press feel |
| Disabled | `--surface-secondary` | `--border-light` | `--text-secondary` | Gray-out |

#### Text Input / Free-Write Textarea
| State    | Background           | Border           | Text             | Notes |
|----------|---------------------|------------------|------------------|-------|
| Default  | `--surface-primary`  | `--border-mid`   | `--text-primary` | |
| Focus    | `--surface-primary`  | `--border-gold`  | `--text-primary` | Gold focus ring |
| Filled   | `--surface-secondary`| `--border-mid`   | `--text-primary` | Subtle fill confirms input |
| Error    | `--surface-warm`     | `--color-bark`   | `--text-primary` | Warm, not clinical red |

#### Progress Indicator (Quiz — question X of 8)
- Font: `--font-utility`, 11px, `--text-secondary`
- Active dot: `--accent-primary` (8px circle)
- Inactive dot: `--border-mid` (6px circle)
- No animation required — static dots update on question advance

---

## 5. Border Radius

| Token      | Value  | Use |
|------------|--------|-----|
| `--radius-sm` | 4px  | Chips, small badges |
| `--radius-md` | 8px  | Buttons, input fields |
| `--radius-lg` | 12px | Option cards, form sections |
| `--radius-xl` | 20px | Full card containers |

---

## 6. Motion / Transition

Minimal. Never distracting. The practice is unhurried — transitions should feel the same.

| Element             | Property         | Duration | Easing          |
|---------------------|-----------------|----------|-----------------|
| Question advance    | opacity + translateY | 280ms | ease-out      |
| Checkbox selection  | border-color, background | 160ms | ease          |
| Button hover        | background-color | 180ms   | ease            |
| Form field focus    | border-color     | 140ms   | ease            |

No bounce, no elastic, no spring. Ease-out on entrances. Ease on state changes.

---

## 7. Primary Mark — Usage Rules

### The Sunburst
The sunburst is the only mark. It appeared independently in both of Anissa's existing card designs without being planned. It is her symbol. It is non-negotiable.

**One sun. Centered. Grounded. Never scattered multiples.**

### Format Variants

| Variant          | Ray Count | Use |
|------------------|-----------|-----|
| Full sun         | All rays  | Primary card (front), signage, any large-format application |
| Simplified sun   | 8 rays    | Small formats — roll-on labels, stamp-size applications |
| Watermark        | 8 rays, low opacity (10–15%) | Background element, document watermark |

### Color Usage

| Ground         | Sun Color       | Notes |
|----------------|----------------|-------|
| Parchment      | Gold Sun `#C8922A` | Standard |
| Linen          | Gold Sun `#C8922A` | Standard |
| Rose Blush     | Gold Sun `#C8922A` | Standard |
| Umber Deep     | Gold Sun `#C8922A` | Maximum contrast — most striking |
| White          | Gold Sun `#C8922A` | Acceptable for digital use |

Never: outline-only sun on a light ground. Never: white sun. Never: sage or bark sun. Gold only.

### Clearspace
Minimum clearspace around the mark: equal to the radius of the center circle on all sides. Nothing crowds the mark.

---

## 8. Voice + Tone Guide

### The Governing Lens
Everything is filtered through the Luminous Steward archetype. She does not announce herself. She holds the lamp. She does not drag anyone toward the light. She makes sure it is there when they are ready.

### Her Aesthetic Language — Use These Words
sacred · embodied · ancient · somatic · sanctuary · received · witnessed · threshold · present · unhurried · honest · alive · nourishing · connected · grounded · deep care · whole · held

### Words to Never Use
| Avoid | Why |
|-------|-----|
| journey / healing journey | Worn to meaninglessness |
| transformative / transformation | Overused, implies before/after sales framing |
| holistic wellness | Wellness industry cliché |
| self-care | Commodified, trivializes what she does |
| competitors | Do not frame anything competitively |
| fix / fixed | She creates conditions — she does not fix people |
| clients (in copy for Anissa) | Use "people" or "the person" instead where natural |
| business problem | Nothing is a problem to solve — it is a gap or an invitation |
| visibility | Do not suggest she needs more of it |
| solution | Too transactional |
| invest in yourself | Overused coaching copy |
| game-changer / life-changing | Hyperbole that undermines the quiet authority |

### Register by Medium

| Medium          | Tone | Notes |
|-----------------|------|-------|
| Business card   | Ancient, precise, minimal | Let the mark and the name do the work |
| Practice bio    | Warm authority | First-person for About, third-person for Bio |
| What to Expect  | Unhurried, reassuring | Address the reader directly as "you" |
| Referral message | Personal, felt, no pitch | Written as if from Anissa to a friend |
| Intake form     | Warm, curious, safe | Clinical language is the enemy here |
| Archetype quiz  | Reflective, invitational | She's asking Anissa to look inward — gentle |
| Pricing doc (internal) | Clear, direct, grounding | Written to give Anissa her spine back |

### Second-Person Throughout
All client-facing copy addresses the reader as "you." Not "our clients." Not "people who come to us." You. It is one person speaking directly to one person.

---

## 9. Routing Mechanism — HTML Tools

### Decision (Locked 2026-05-23)
All interactive HTML tools (archetype discovery quiz, client intake form) route results to Michael Muyot via `mailto:` link pre-populated with encoded responses. A clipboard copy button is provided as a fallback.

### Implementation

**Quiz results (routes to Michael):**
```
mailto:michael@apexdao.io?subject=Anissa%20Archetype%20Discovery%20Results&body=[encoded-answers]
```

**Intake form (copy to Michael + Anissa's use):**
```
mailto:michael@apexdao.io?subject=New%20Client%20Intake&body=[encoded-form-fields]
```

**Clipboard fallback:**
A "Copy to send" button copies the full formatted results text to the user's clipboard. Label: "Copy results to send" — never "Submit" or "Send" (those imply server-side behavior that doesn't exist).

### Encoding
Use `encodeURIComponent()` to encode all field values before appending to the `mailto:` href. Build the body string in JavaScript on button click, not on page load — prevents stale data.

---

## 10. Accessibility Baseline

All HTML tools meet these minimums:

- All form inputs have associated `<label>` elements
- Focus states are visible (gold border, 2px minimum)
- Color is never the only indicator of state (border + background both change)
- Font size minimum: 12px (no exceptions)
- Tap targets minimum: 44px height on all interactive elements (neurospicy requirement)
- Free-write fields have placeholder text that gives an example, not a command

---

*Anissa Russell Brand Token Spec // v1.0 // Locked 2026-05-23 // Prepared by Michael Muyot*
*All downstream deliverables reference this document. Do not build HTML tools or print specs without it.*
