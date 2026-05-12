<!-- SEED: re-run /impeccable document once there's code to capture the actual tokens and components. -->
---
name: jrgmadrid.dev
description: After-hours editorial for a developer who reads. Brand register, committed color, two-register typography.
---

# Design System: jrgmadrid.dev

## 1. Overview

**Creative North Star: "The Late-Tokyo Editorial"**

A developer's landing in the register of an after-hours periodical. Brutus on a hotel desk at 11pm, Vogue China at the airport newsstand on the way back, TEETH dog-eared on the nightstand. The closest web-native analog is **Screen Slate**: independent repertory-cinema publication, heavily typographic, asymmetric calendar-style layouts, restrained color, no SaaS-cream concessions to legibility-by-template. The page commits to a single color (deep night-sky purple from the riverside scene in *Night Is Short, Walk On Girl*) and pairs an editorial display face with a monospaced body, letting the cultivated and technical registers sit in the same voice without negotiating with each other. Motion is restrained; the page rewards the reader who scrolls slowly.

The bar is not "good dev portfolio." The bar is *this month's issue of Brutus on the side table*. The system explicitly rejects the dev-portfolio lanes named in PRODUCT.md: the SaaS-cream Stripe-clone, the AI-startup purple-gradient, the Linear-clone dark-mode-with-glass, the theatrical character-forward register that belongs to morningstar.moe, and the techbros-doing-taste tinted-tasteful that PRODUCT.md actively defends against. The night-sky purple is a *committed* surface color, not an accent: anywhere it shrinks below 30% of the screen, the design has lost the bet.

**Key Characteristics:**

- Committed night-sky purple owning 30–60% of every screen.
- Two-register type pairing: editorial display + monospaced body.
- Restrained motion. State changes only. No scroll-driven choreography.
- Density as feature. Body type earns its keep; layout rhythm comes from variation, not uniformity.
- Print-magazine references (Brutus, Vogue China, TEETH) over dev-portfolio references.

## 2. Colors: The Night-Sky Palette

A committed strategy: one saturated color carries the surface, anchored by tinted neutrals. The character is a deep, blue-leaning, low-to-moderate-chroma purple: the upper-sky color in the riverside frame from *Night Is Short, Walk On Girl*, not the AI-startup purple lane.

### Primary

- **Night-Sky Purple** (anchor: oklch(28–32% 0.08–0.10 285) range; exact value resolved during implementation against on-screen rendering and contrast tests): Owns the dominant surface. The brand IS this color. Specifically distinct from the high-chroma violet-magenta lane of AI/crypto aesthetics; this is deep and slightly desaturated, the color of a sky that has been dark for two hours.

### Neutral

- **Tinted whites and warm-grays** (to be resolved during implementation; chroma 0.005–0.01 toward the brand hue, never pure `#fff` or `#000`): Used for body text, secondary surfaces, dividers. Every neutral carries a trace of the brand hue so the page never reads as "purple plus default Tailwind grays."

### Secondary (held in reserve)

A single warm pop may emerge during implementation: the yellow cardigan / red ribbon / cherry-blossom-pink contrast against the deep purple in the source frame suggests there's room for one warm accent if a moment demands it. Used at ≤5% of any screen. Not introduced unless earned.

### Named Rules

**The Committed Color Rule.** The night-sky purple is not an accent. It is the surface. Anywhere this color is reduced to a small percentage of the layout, the design has retreated to Restrained and should be reconsidered.

**The Anti-AI-Purple Rule.** The anchor is *deep night-sky*, not *Stable-Diffusion-default*. If the purple reads as bright, violet-pink, gradient-saturated, or accompanied by cyan glow, it has drifted into the lane PRODUCT.md actively rejects. Pull it back toward navy-leaning, lower-chroma, *atmospheric*.

## 3. Typography: The Two-Register Pairing

**Display Font:** [Editorial display family, to be chosen at implementation. Candidates worth probing: a refined serif like GT Sectra, Tiempos, or Söhne Breit; or a distinctive sans like Söhne Mono Buch's display weights, Reckless, or PP Editorial New.]

**Body / Label Font:** [Monospaced family, to be chosen at implementation. Candidates worth probing: JetBrains Mono, IBM Plex Mono, Berkeley Mono, GT America Mono, Söhne Mono.]

**Character:** A two-register pairing. The display face carries the cultivated voice (criticism, periodicals, the books on the desk). The monospaced body carries the technical specificity (claude, mastra, kafka, owner-verbs, "killed a 5–10s lag"). The pairing IS the brand: cultivated and internet-native in the same voice, the same way the source person operates across surfaces.

### Hierarchy

- **Display** (heavy weight, large clamp scale): Hero headlines and section openers. Sparing: the rare large-typographic moment, not the default.
- **Headline** (display, medium weight, mid scale): Subsection markers, important asides.
- **Title** (display or mono depending on context, medium weight): Project titles, post titles.
- **Body** (monospace, regular weight, 14–16px, line-height ~1.6, max 65–75ch): Paragraph text. Density rewards reading.
- **Label** (monospace, smaller, possibly with letter-spacing if uppercase): Metadata, timestamps, captions, footnotes.

### Named Rules

**The Two-Register Rule.** Display carries the cultivated voice; mono carries the technical specificity. Neither face does both. If a use of type doesn't clearly belong to one register, it doesn't belong on the page.

**The Lowercase-By-Default Rule.** Body and label copy is lowercase unless capitalization carries meaning (proper nouns, code identifiers, acronyms). Sentence-case prose reads as performing seniority. Lowercase reads as past needing to. This is a brand-voice rule from PRODUCT.md made typographic.

**The Density Rule.** Body text is allowed to be dense. Long paragraphs, footnotes, asides. The page does not pad. Surface clarity for the skimmer is achieved through hierarchy and white space *between* sections, not through diluting the text within them.

## 4. Elevation: Flat-by-Default

The system is flat at rest. Depth is conveyed through type weight contrast, color blocking against the committed purple surface, and rule lines (1px dividers, occasional horizontal rules). Cards are the lazy answer and are not the default container; most content does not need a card around it.

Motion is restrained (state changes only: hover, focus, click), so the page does not need decorative layering to feel alive.

### Named Rules

**The Flat-By-Default Rule.** Surfaces are flat at rest. Shadows appear only as a *response* to interaction (hover, focus), never as decoration. If a shadow is doing aesthetic work rather than functional work, it has failed the test.

**The No-Card-By-Reflex Rule.** Cards are only used when a true affordance demands them (a clickable container with distinct hover state). Most content lives on the surface directly, separated by spacing and rule lines. Nested cards are forbidden.

## 5. Components

Seed mode. No components yet. Real component patterns (buttons, links, navigation, the rare card, code blocks, footnote markers) emerge during implementation. Re-run `/impeccable document` after the landing page is built to capture the actual primitives and write the `.impeccable/design.json` sidecar.

## 6. Do's and Don'ts

### Do:

- **Do** commit to the night-sky purple as the dominant surface (30–60%, not a 7% accent). The Committed Color Rule.
- **Do** pair editorial display with monospace body. The Two-Register Rule.
- **Do** carry the references in spirit: Brutus (typographic confidence, dense editorial layouts, full-color commitment), Vogue China (mixed-script typographic rhythm, photo-forward but type-anchored), TEETH (independent-editorial sensibility), and **Screen Slate** (the one web-native reference: editorial layout principles translated to the browser without surrendering to web defaults). Print over web; magazine over portfolio.
- **Do** use lowercase as the default register for body and label copy. The Lowercase-By-Default Rule.
- **Do** let body text be dense. Density rewards reading. Surface clarity comes from hierarchy and section-level whitespace, not from short-paragraph dilution.
- **Do** flat by default. Shadows respond to interaction; they do not decorate at rest.
- **Do** treat the night sky from *Night Is Short, Walk On Girl* (riverside scene) as the canonical color reference. When in doubt, look at the frame.

### Don't:

- **Don't** treat the purple as decorative. If the page can lose it without losing the brand, it isn't committed.
- **Don't** drift into AI-startup purple territory: bright violet-pink, gradients, cyan accents, glow borders. *Stable-Diffusion-default* is the anti-anchor. The Anti-AI-Purple Rule.
- **Don't** look like a **Generic SaaS dev portfolio**: Inter / Geist / Plus Jakarta, hero + skill icons + project cards + footer. The Vercel/Tailwind landing template look. (PRODUCT.md anti-reference.)
- **Don't** clone the **Crypto / AI-startup aesthetic**: purple/violet gradients, cyan-on-dark, glassmorphism, animated mesh backgrounds, gradient text. (PRODUCT.md anti-reference.)
- **Don't** clone **Linear**: dark UI with glass cards, blurred backgrounds, gradient borders, "designed by an eng who likes Linear." (PRODUCT.md anti-reference.)
- **Don't** drift **theatrical or character-forward**: mascots, illustrations, big personality animations. That register lives on morningstar.moe, not here. (PRODUCT.md anti-reference.)
- **Don't** fall into the **techbros-doing-taste** lane: Stripe-clone restrained-tasteful, "I learned about Helvetica recently," stoicism-as-personality, founder-shelfie taste. The cited dislike (*thinking you have "taste" just because you've read marcus aurelius once*) is defended against actively. (PRODUCT.md anti-reference.)
- **The Not-By-Default Rule.** **Don't** ship anything that could have been generated by any other Claude session asked for a developer landing page. The reflex set: Inter / Geist / Plus Jakarta as default sans, shadcn-style cards (rounded-lg + shadow-sm + 1px gray border), lucide-react as the universal icon language, the Tailwind default gray/zinc/slate ramp, the "hero + three-feature grid + CTA + footer" structural template, purple-violet gradient CTAs, glassmorphic accents, decorative single-label monospace, "Built with X" footer badges, centered hero on a gradient. The fact that Claude is writing this DESIGN.md does not change the bar; if anything, knowing what the model's defaults are makes refusing them more rigorous. The test: open the rendered page and ask whether any other agent session, given the same prompt, would output something visually adjacent. If yes, the design has failed.
- **Don't** use side-stripe `border-left` accents (>1px colored stripes on cards/callouts/list items). Cross-register absolute ban.
- **Don't** use `background-clip: text` with gradients. No gradient text. Cross-register absolute ban.
- **Don't** default to glassmorphism. Rare and purposeful, or nothing. Cross-register absolute ban.
- **Don't** ship a hero-metric template (big number + small label + supporting stats + gradient accent). SaaS cliché. Cross-register absolute ban.
- **Don't** ship identical card grids (same-sized cards with icon + heading + text repeated endlessly). Cross-register absolute ban.
- **Don't** animate CSS layout properties (width, height, padding, margin). Use transform and opacity. Cross-register absolute ban.
- **Don't** use bounce or elastic easing. Exponential ease-out curves only.
- **Don't** use em dashes in copy. Commas, colons, semicolons, periods, or parentheses. Also not `--`.
- **Don't** wrap everything in containers. Most things live on the surface directly.
