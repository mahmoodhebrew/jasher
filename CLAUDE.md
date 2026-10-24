# جسر (Jasher) — منصة تعليم العبري للناطقين بالعربية

## What this is
An interactive Hebrew-learning platform for Arabic speakers. The whole site is one file, `index.html` (HTML + CSS + JS inline), published with GitHub Pages from `main`. Pushing to `main` updates the live site, so keep `main` working.

## Learners
- Arab citizens who already know some Hebrew, and learners from the West Bank / Jerusalem starting from zero.
- Goal: speaking, understanding, reading and writing.
- Most use a phone: design mobile-first, RTL (`dir="rtl"`, `lang="ar"`); Hebrew text gets its own `lang="he"`.

## Content rules (must follow)
- **No personal details about the owner anywhere on the site**: no name, no mention of nursing studies, nothing about him.
- Explanations in **simple Modern Standard Arabic**; dialogues and tips in **Palestinian colloquial Arabic**.
- Nursing track (owner decision, Oct 2026): translations of Hebrew lines (flip cards) are in **accurate MSA**; only the mentor's tips stay colloquial.
- **No recorded lessons.** Everything is interactive: dictionary, flashcards, sentence completion, many exercise types. Learning should feel enjoyable.
- Teaching only, **no exam prep** for now.
- Unit 1 covers the **whole alphabet in parts**, with both **print and handwritten (cursive)** forms.
- Tracks: general Hebrew first (basics), then the **nursing** track. More professions later.
- Audio: AI / browser voice (`speechSynthesis`) for now.

## Technical rules
- Keep it a static site: no build step, no backend, no frameworks unless the owner agrees.
- Progress is saved in `localStorage`; wrap reads/writes in try/catch and never break old saved progress.
- Reuse the existing CSS variables (`:root` palette) and components instead of adding new ones.
- The owner works only from a phone/iPad: explain changes in short, simple Arabic, and say what to check on the live site.
- Before committing, sanity-check that `index.html` still loads (no JS syntax errors).

## Tools in this repo
- Skills from Agent Skills and Ponytail are in `.claude/` (`/spec`, `/plan`, `/build`, `/review`, `/ponytail-review`).
- Prefer the smallest change that fully solves the task (Ponytail), but never cut accessibility or input validation.
