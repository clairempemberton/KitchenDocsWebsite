# Nellie — brand identity for Smart Kitchen Docs

Design spec, 2026-09-18. Status: approved direction, not yet implemented.

## The problem

The site is committed to a cold identity and says so in its own README: "data-plate
motif, porcelain/graphite palette, gas-flame blue accent." Every choice reinforces
*machine*.

- **The palette contains no warm hue at all.** Ground `#E9EBE8`, body text `#4E565B`,
  accent `#1652C8`. This is doing more of the stiffness than the fonts or the mark.
- **The type is industrial.** Archivo condensed plus Martian Mono reads as spec sheet
  and terminal.
- **The mark is a rivet plate** — an object bolted to the back of a machine.
- **The voice has no subject.** "43 units / 61 manuals / 2,200+ pages / 100% cited"
  is inventory, not a promise.

The product is opened by a stressed kitchen manager at 6am with a unit down. Cold
precision is not reassuring in that moment; it is one more manual.

## Positioning

Restaurant back-of-house software is uniformly sober — Toast, 7shifts and MarginEdge
are all wordmark-and-gradient. No competitor has a character. B2B mascots are a
validated tactic (Salesforce Astro, Snyk's Patch, Moz's Roger), and the consistent
lesson is *position first, mascot second*: the animal has to mean the value
proposition.

Ours does. An elephant never forgets — which is the product. Every manual, every
service interval, retained and produced on demand.

## Naming architecture

The company name does not change.

| Layer | Name | Rationale |
|---|---|---|
| Company / domain / SEO | **Smart Kitchen Docs** | Keeps the descriptive search equity and B2B credibility already owned |
| The assistant | **Nellie**, an elephant | Gives the brand a face, a verb ("ask Nellie") and somewhere to put warmth |

### Why "Nellie" and not "Elly"

"Elly" was the starting instinct and had to be rejected on research:

- `elly.ai` is a funded AI hiring platform that brands itself explicitly as an
  "AI assistant."
- "C1 Elly" is an enterprise generative-AI assistant platform.

Not a legal blocker — the trademark is "Smart Kitchen Docs," and food-service software
is a different class from recruiting software — but being the third AI assistant named
Elly costs the search result and undercuts the "she's ours" feeling the mascot exists
to buy.

"Nellie" is clean in this space, carries elephant heritage through the 1956 children's
song (whose UK phrase trademark was revoked for non-use), and reads warm and
old-soul rather than tech.

**Spelling is "Nellie," not "Nelly."** In the US "Nelly" is overwhelmingly the rapper.

**Rejected outright: "Peanut."** A perfect elephant name and a top-9 allergen on every
screen of a food-service product.

### Trademark follow-up

`Aunt Nellie's Foods, Inc.` holds food-class marks (canned vegetables). Confusion is
unlikely — a jar of beets versus a character inside back-of-house software — but log it
for counsel at filing time. It does not change the design.

## Scope: where Nellie appears

This is the guardrail that keeps the rebrand professional. It is deliberately narrow,
and deliberately expandable later.

**She appears in:** favicon, app icon, nav mark, hero, occasional section openers,
social avatars, sales deck, merch.

**She does not appear in:** answers, the maintenance list, or any surface a user is
working on. The product UI barely changes in this pass.

**She does not speak.** No first person, ever. Copy stays factual and professional;
third person is allowed but used sparingly. The warmth is carried by palette, type and
mark — not by a character narrating at someone whose oven is down.

The "trunk" metaphor (an elephant's trunk both holds everything and hands you what you
need) stays a light marketing touch in this pass. Promoting it to feature naming
("Nellie's Trunk" as the manual library) is explicitly deferred.

## Palette

Warmth comes from the ground and the text; trust comes from the blue already owned.
The accent moves from electric to soft rather than changing hue.

| Token | Now | New | Role |
|---|---|---|---|
| `--paper` | `#E9EBE8` | `#FBF7F0` | Warm paper ground |
| `--paper-deep` | `#DFE3DF` | `#F2EADD` | Soft oat, section banding |
| `--panel` | `#F6F7F5` | `#FFFDF9` | Cards |
| `--ink` | `#14181B` | `#2A231E` | Warm charcoal, headings |
| `--body-text` | `#4E565B` | `#6E625A` | Warm taupe |
| `--muted` | `#7A8288` | `#8E8279` | Warm muted |
| `--blue` | `#1652C8` | `#3A72D4` | Button and fill accent |
| `--blue-text` | — | `#2C60C4` | **Link and accent text only** — see accessibility |
| `--blue-deep` | `#103F9C` | `#24509E` | Hover |
| `--nellie` | — | `#6FA8E8` | Her body; also light accent |
| `--amber` | `#B67512` | `#D98A29` | Safety / maintenance thread, **fills only** |
| `--amber-text` | — | `#8F5A0D` | Safety thread when it must be text |

`--flame-hot`, `--on-dark*` and the dark-section tokens carry over, rewarmed to match.

### Accessibility — checked, with one real finding

Contrast against the new `#FBF7F0` ground:

| Pair | Ratio | Verdict |
|---|---|---|
| `#2A231E` ink | ~15:1 | Pass |
| `#6E625A` body | 5.53:1 | Pass AA |
| `#3A72D4` blue as text | **4.34:1** | **Fails AA (4.5) — do not use for text** |
| `#2C60C4` blue-text | 5.50:1 | Pass AA |
| White on `#3A72D4` fill | 4.63:1 | Pass AA |
| `#D98A29` amber as text | ~3.5:1 | **Fails AA — fills and icons only** |

The split between `--blue` (fills) and `--blue-text` (text) is not optional. Using the
button blue for link text fails AA on the new ground.

## Typography

| Role | Now | New | Why |
|---|---|---|---|
| Display | Archivo | **Fraunces** | Variable serif with real `SOFT` and `WONK` axes — engineered for warm-but-crafted. Free on Google Fonts. Highest-leverage single swap. |
| Body | Instrument Sans | **Instrument Sans** — keep | Already a good neutral, already loaded. Don't spend risk here. |
| Mono | Martian Mono | **Courier Prime** | Martian Mono reads *terminal*. We quote a **printed manual**. Typewriter mono makes a citation feel like paper and ink — like evidence — rather than like code output. Same rigor, different register. |

## The mark

Drawn original, in the spirit of the reference Dylan supplied — not derived from it.

**Keep from the reference:**
- Thick, even contour line. Survives shrinking, one-colour sticker printing, embroidery.
- Flat fill, no gradient. Same reason.
- Full body, side profile, trunk raised — the pose everyone reads as good news, and it
  gives us something to animate later.
- Small eye, small smile. Restraint in the face is what keeps it out of kids'-app territory.

**Change from the reference:**
- **No gloss highlights.** The white shine strokes are what make it read clipart.
- **Tighten proportions ~15% toward realistic.** The reference is chibi — very large
  head, very stubby legs. Closer to Moz's Roger than a nursery decal.
- **Halve the interior strokes.** Ear fold, leg separations and tail tuft mud up at
  16px. The favicon version is the same character drawn with about half the lines.

**Lockups:**
1. Head-only in a rounded squircle — favicon, app icon, avatar.
2. Full body + "Smart Kitchen Docs" set in Fraunces — nav, footer, deck.

**Favicon rule carries over from the current `favicon.svg`:** it is drawn a touch
heavier than the inline mark because fine strokes vanish at 16px. Keep that comment and
keep changing both together.

**Artwork ownership:** the reference image appears to be stock or AI output. Nellie must
be original artwork we own outright, or she cannot go on merch, in an App Store listing,
or into a trademark filing.

## The data plate does not die — it demotes

The rivet-plate motif stops being the logo and becomes the **citation chip**: every
cited manual quote sits in a small riveted plate, set in Courier Prime, with its page
number.

This keeps the rigor visible exactly where it earns trust, removes it from everywhere it
was only making the site cold, and makes the rebrand read as an evolution of the site's
own language rather than a replacement of it.

## Voice

Same claims, same precision, warmer construction. Nellie may be referenced; she never
speaks.

| Now | After |
|---|---|
| "Ask a plain-language question about any unit in your commercial kitchen and get the answer straight out of the manufacturer manual, with the page it came from." | "Every manual for every unit you own, read and indexed. Ask a question, get the answer — and the page it came from." |
| "43 units / 61 manuals / 2,200+ pages / 100% cited" | "43 units · 61 manuals · 2,200 pages. Every answer cited." |
| "Reads each manual's service intervals into a maintenance schedule you approve" | "Service intervals, found in the manuals and brought to you to approve. Nothing invented." |

Tone rules:
- Short declaratives. No exclamation marks.
- Never invent capability — the README's warning about the `.next` strip stands, and the
  rebrand must not blur what is shipped versus what is not.
- The single CTA stays **Book a walkthrough** until the app store listings are live.

## Files touched

| File | Change |
|---|---|
| `index.html` | Token block, font links, mark SVGs, hero, section openers, copy pass |
| `doc.css` | Same token and type changes for the secondary pages |
| `favicon.svg` | Replace the data plate with the Nellie head mark |
| `privacy.html`, `support.html` | Inherit via `doc.css`; header mark swap |
| `README.md` | Rewrite the identity paragraph — it currently documents the old motif |
| new asset files | Nellie SVGs (full body, head, favicon weight) |
| `index.html` meta | `theme-color` `#E9EBE8` → `#FBF7F0` |

No build step, no dependencies. That does not change.

## Out of scope for this pass

- Nellie in the product UI (answers, maintenance list, empty states).
- First-person voice or any Nellie dialogue.
- "Nellie's Trunk" as feature naming.
- Completion celebrations and sleeping/idle states.
- An `og:image` — still blocked on real app screenshots, per the README.
- Animation.

Each is a deliberate later option, unlocked only if the face earns it.

## Open items

- [ ] Original Nellie artwork commissioned or drawn; confirm we own it outright.
- [ ] `Aunt Nellie's Foods` logged for counsel at filing time.
- [ ] Re-verify every contrast pair against final hexes before ship.
