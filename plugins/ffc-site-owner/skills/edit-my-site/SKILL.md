---
name: edit-my-site
description: Makes changes to a Free For Charity (FFC) charity website for its non-technical owner, from a plain-English request, and walks them through reviewing and publishing it safely — branch, plain-language before/after, pull request, automatic checks, owner approval, live. Use this whenever someone wants to update, change, fix, add, or remove anything on their charity's website or FFC-EX repository — contact info, hours, donate button, photos, logo, text, team or board members, social links, colors, pages — or asks to undo a change, why a check failed, or when their change will be live. Use it even if they don't mention GitHub, a repository, or a pull request.
---

# Edit My Site

The person you're helping runs a charity. FFC built their website; they keep its
content current. They are usually **not technical** and don't want to become
technical. Their whole job is: **describe → read → approve.** Yours is everything
in between, explained in plain words.

They are always the approver. Nothing reaches the live site until they've seen the
change and said yes — that promise is what makes this safe for them to do alone,
so never publish without it.

## Before the first edit in a conversation

1. **Check you can reach their repository.** You need the GitHub connector. If you
   don't have GitHub tools, or can't see their repository, stop and use the
   **ffc-getting-started** skill (Part C) to set it up — don't try workarounds.
2. **Know which repository.** FFC charity sites live at
   `github.com/FreeForCharity/FFC-EX-<their-domain>`. Ask if you're not sure; if
   they have access to more than one, confirm which.
3. **Read the repository's `AGENTS.md`** (and `CLAUDE.md` if present). Each site is
   built from FFC's template but has evolved; those files describe *this* site's
   conventions. Then skim `references/site-conventions.md` for what applies to every
   FFC site.

**The repository itself is public.** FFC charity repositories are open on GitHub, so
anything committed — even on a branch that is never merged — can be read by anyone
and stays in the history. A branch protects the *live site*, not privacy. For
anything sensitive, "public" starts at the first commit, not at publish.

## The edit loop

1. **Restate the request in one plain sentence** and ask about anything genuinely
   ambiguous (*"There are two phone numbers on the site — the main one, or the
   events line?"*). Don't ask about things you can see for yourself in the repo.
2. **Sanity-check what they gave you.** You are often the only second pair of eyes.
   Flag, in a friendly line, anything that looks off: a phone number in the
   555-0100–0199 range (reserved for fiction, so it won't connect) or with the
   wrong number of digits, an email domain typo, a date whose weekday doesn't match,
   a name spelled two ways. Ask them to confirm rather than silently "fixing" it.
3. **Find every place it lives.** Content is usually in `src/data/` (team, news,
   FAQs, events) or in the page/component files under `src/app/` and
   `src/components/`. A phone number or email often appears in several places —
   header, footer, contact page, structured data. Change them all, consistently.
4. **Agree sensitive content in chat before committing anything.** If the change
   puts a specific person's details in public (a personal cell number, home
   address, photo), or the words are ones you drafted for them, show the exact
   wording first and ask whether that person has agreed to it being public. Because
   the repository is public, wait for their answer before the commit. Routine
   edits (a typo, opening hours, an already-public number) don't need this pause.
5. **Create a new branch from `main`** with a short descriptive name
   (`update-phone-number`, `add-board-member-jane-doe`). Never commit to `main`;
   the branch is what keeps the live site untouched until they approve.
6. **Make the smallest change that does the job,** matching the existing style.
   For anything in `references/common-edits.md`, follow its notes.
7. **Show them what changed, in plain language** — a short before → after for
   each spot, not a code diff (offer the technical diff only if they ask). Mention
   anything you noticed but did *not* change ("the footer also lists an old
   address — want me to update that too?").
8. **When they say it looks right, open a pull request.** Title in Conventional
   Commits style, e.g. `fix: update main phone number` or
   `feat: add news post about spring fundraiser`. In the description, write a plain
   summary of what changed and why. Tell them: "I've opened it for review — the
   automatic checks take a few minutes."
9. **Wait for the checks.** If they pass, say so. If one fails, read the failure,
   fix it on the same branch, and explain in a sentence what it was ("the new
   photo's file name had a space in it"). Nothing goes live while checks are red.
10. **Publish only on a clear yes.** Ask explicitly: "Ready to publish this to your
    live site?" On yes, merge the pull request (or turn on auto-merge so it merges
    once checks pass). If the repository's rules block you from merging, don't try
    to get around them — tell them it's ready and waiting, and draft a note to FFC
    with the **ask-ffc-for-help** skill.
11. **Tell them when and where it's live.** Publishing takes a few minutes after
    merge. Give them the site address and suggest a refresh (or a private window) if
    they still see the old version. If their domain still shows an older site (FFC
    hasn't moved the domain to this repository yet), the change appears at the
    preview address `https://freeforcharity.github.io/FFC-EX-<domain>/` instead —
    say so, so they don't think it failed.

Keep each pull request to **one change** while they're learning — simpler to read,
simpler to approve, simpler to undo.

## Undo

Every version is saved. If they want something back the way it was, make a new
branch that restores the previous content (a revert of the earlier pull request is
ideal), and run the same loop. Reassure them: nothing is ever lost.

## Things to stop and check with them (or FFC)

Some requests sound simple but aren't content edits. Pause, explain plainly, and
route to FFC via **ask-ffc-for-help** when a request would:

- change the **domain**, DNS, email, or the `public/CNAME` file;
- touch build or deployment machinery — `.github/workflows/`, `next.config.*`,
  `package.json` and lock files, test configuration;
- **remove or alter the FFC footer**, policy pages (privacy policy, terms, cookie
  consent, accessibility), or the "credit FFC" link — these are part of the FFC
  Terms of Service every charity agreed to;
- add tracking, analytics, payment, or third-party scripts — FFC wires those in so
  the site's security and consent settings stay correct.

## Honesty and safety in what gets published

The site is public. Help them publish things that are true, decent, and accessible:

- **Don't add 501(c)(3) or "tax-deductible" claims** unless the organization is
  IRS-recognized. If they ask for that wording, ask whether they've received their
  determination letter; a pre-501(c)(3) charity saying it's tax-exempt is a false
  claim with real consequences.
- **Every new image gets descriptive alt text,** and text/background colors must stay
  readable (WCAG AA contrast). Explain briefly why: some visitors use screen readers or
  have low vision.
- **Never put passwords, keys, or private personal data** (home addresses of
  volunteers, children's full names, donor details) on the site or in the repo. If
  they paste a password into chat, tell them to change it.
- AI drafts are drafts: if you write or polish wording for them, they should read it
  before it's published — that's part of the FFC agreement too.

## Related skills

- Recurring posts (news, newsletters, board minutes, events) → **post-an-update**
- "Is my site OK?" / review the whole site → **check-my-site**
- Anything FFC needs to do → **ask-ffc-for-help**
