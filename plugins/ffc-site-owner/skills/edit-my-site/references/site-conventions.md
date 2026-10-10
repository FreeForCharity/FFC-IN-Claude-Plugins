# Conventions shared by FFC charity sites

The repository's own `AGENTS.md` / `CLAUDE.md` wins wherever it differs from this
file — sites evolve after they're created from the template.

## What the site is

- **Next.js** (App Router) with **TypeScript**, styled with **Tailwind CSS**, exported
  as a **static site** and hosted on **GitHub Pages**.
- Before the domain is connected, the site lives at
  `https://freeforcharity.github.io/<repo-name>/`; afterwards at the custom domain.
  Both must work — which is why asset paths matter (below).
- Merging to `main` triggers the build and deploy automatically. The required check
  is typically named **"Build, Test, and Verify"** (some repos split it into
  separate lint/test/build jobs).

## Where content usually lives

| Content | Typical location |
|---|---|
| News / blog posts | `src/data/news/` — one file per post plus an `index.ts` that lists them |
| Team / board | `src/data/team.ts` or `src/data/team/` |
| FAQs, testimonials, events | `src/data/faqs.ts`, `testimonials.ts`, `events.ts` |
| Page text | `src/app/<route>/page.tsx` and section components in `src/components/` |
| Footer | `src/components/footer/` |
| Images | `public/Images/` (some repos use `public/images/`) |

Always look at a neighbouring example (an existing post, an existing team member)
and copy its shape rather than inventing a new one.

## Rules that break the site if ignored

- **Images and other files in `public/` must be referenced through the
  `assetPath()` helper** from `src/lib/assetPath.ts` (e.g.
  `assetPath('/Images/board/jane-doe.jpg')`), not a bare `/Images/...` path. A bare
  path works on the custom domain but breaks on the GitHub Pages preview address.
- **Route folders are kebab-case**: `src/app/board-minutes/page.tsx`, never
  `boardMinutes` or `board_minutes`. File names for images: lowercase, hyphens, no
  spaces (`spring-gala-2026.jpg`).
- **New pages go in the sitemap/navigation** the way existing pages do — check how
  `src/app/sitemap.ts` and the header/nav list routes, and follow suit.
- Keep text in the existing **data files** rather than hard-coding it into
  components when a data file exists for it.

## Images from the owner

When they provide a photo: save it under `public/Images/` with a descriptive
kebab-case name; prefer `.jpg`/`.webp` for photos and keep large photos reasonably
sized (around 1600 px on the long edge is plenty). Ask them for alt text if the
content of the photo isn't obvious, or propose one and let them confirm.
If you can't upload binary files through the tools available, say so plainly and
suggest they upload it via the GitHub website's "Add file → Upload files" on your
branch, or send it to FFC.

## Don't touch without FFC

`.github/`, `next.config.*`, `package.json` / lock files, `public/CNAME`,
test and lint configuration, the cookie-consent and analytics setup, and the FFC
footer structure. These keep the site building, secure, and compliant.
