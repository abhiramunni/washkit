# WashKit — Laundry, Sorted

Laundry day, without the guesswork. WashKit keeps your wash pile on a virtual
clothesline, plans your wash days, decodes any care label, rescues stains step
by step, shows what each load really costs, and tells you whether today is a
good drying day in Bengaluru.

Live: https://abhiramunni.github.io/washkit/

## What it does

- **The Line** — every garment you own hangs on a clothesline with a
  Fresh / Due soon / Wash now tag. Tap **Washed** and its clock restarts.
  Add your own clothes; the line grows with you.
- **Wash-day planner** — pick your wash days (Wed & Sat by default), tick
  loads off as they go in the machine, and watch the countdown to the next
  wash day. The week resets itself every Monday.
- **Care-symbol decoder** — all 24 standard laundry symbols (wash, bleach,
  dry, iron, dry clean), drawn the way they look on the tag, each with a
  plain-words meaning and what to do.
- **Stain SOS** — 8 common stains (turmeric, chai, oil, ink, sweat, mud,
  blood, red wine) with step-by-step rescue instructions and a "never do"
  warning. Golden rule: cold water first — heat sets a stain.
- **Cost checker** — what one load really costs at home: detergent + power +
  water at Bengaluru rates (about ₹12.70 a load at 4 loads a week), compared
  with hand-washing and the laundry shop. Sliders for loads, detergent price,
  dose and power tariff.
- **Drying forecast** — live Open-Meteo data for Bengaluru (rain chance,
  humidity, cloud, wind) turned into a plain verdict: good day, slow day, or
  keep it indoors. Falls back gracefully when offline.
- **Guides** — six plain-language laundry lessons: sorting, detergent dosing,
  keeping whites white, stopping shrinkage, monsoon drying, ironing.

## The maths (defaults, all labelled as estimates)

- Machine load: detergent ₹220/kg × 30 g = ₹6.60, power 0.8 kWh × ₹7 = ₹5.60,
  water 50 L ≈ ₹0.50 → **₹12.70 per load**
- 4 loads a week → ₹220 a month, ₹2,642 a year
- Hand wash: ₹3.60 a load → ₹62 a month
- Laundry shop: ₹80/kg × ~4 kg a load → ₹320 a load, ₹5,542 a month

## Tech

- One self-contained `index.html` — no backend, no signup, no build step.
- Data lives in `localStorage` only. Copy a summary, remove the samples, or
  erase everything with two taps.
- Warm editorial palette (ivory paper, espresso ink, bronze and terracotta),
  Fraunces + Inter, cinematic intro with tap-to-skip, 3-step onboarding tour.
- Drying forecast uses the Open-Meteo API (no key); everything else works
  fully offline.

## Files

- `index.html` — the whole app (photos embedded)
- `index-publish.html` — the published version (photos as repo-root files)
- `washkit-hero.webp`, `washkit-flatlay.webp` — AI-generated warm-editorial photos
- `qa-test.js` — headless jsdom QA (60 assertions, all passing)
- `chunks/` + `build.py` — the 10 source chunks and the assembler
- `pubchunks/` + `split-publish.py` — the publish chunks for the GitHub web editor

## Privacy

Nothing leaves the browser. No accounts, no tracking, no uploads.
