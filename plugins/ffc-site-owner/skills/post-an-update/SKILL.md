---
name: post-an-update
description: Publishes recurring content on a Free For Charity (FFC) charity website — news or blog posts, announcements, monthly newsletters, board meeting minutes, upcoming events, photo recaps — creating the section the first time if the site doesn't have one yet. Also helps the owner turn rough notes, an email newsletter, or meeting notes into a post that's ready for the site. Use this whenever someone wants to post, publish, share, or announce something on their charity's website, put the newsletter or minutes online, add an event, or start a blog — even if they just paste some text and say "can this go on the site?".
---

# Post an Update

Charity sites grow by adding posts over time: news, newsletters, minutes, events.
This skill decides **what** to publish and **where**; the branch → review →
approve → publish mechanics are exactly those of the **edit-my-site** skill — follow
its loop and guardrails for the actual change.

## 1. Understand the post

Get, or ask for only what's missing:
- **Type** — news/blog post, newsletter issue, board minutes, event, photo recap
- **Title** and **date** (for events: date, time, place, and how to RSVP/register)
- **Content** — their text, a pasted email newsletter, a document, or notes
- **Images**, if any, with alt text

If they hand you rough notes and ask you to write it up, draft it in their charity's
voice (look at existing posts), keep it concise and factual, and **show them the draft
before it goes into the site**. They approve the words, not just the code — FFC asks
every charity to review AI-written content before publishing.

## 2. Find, or create, the right section

Look at the repository first (read `AGENTS.md`):

- **Section exists** (e.g. `src/data/news/` with one file per post and an
  `index.ts`) → add the new entry in exactly the same shape as the most recent one,
  newest first, and keep earlier entries listed.
- **No section yet** → propose creating one: a listing page plus individual entries,
  styled like the rest of the site, a kebab-case route (`/news`, `/newsletter`,
  `/board-minutes`, `/events`), linked from the main navigation or home page, and
  added to the sitemap the way other pages are. Tell them what you're about to
  create in one or two sentences before doing it — a new section is a bigger change
  than a post.

## 3. Content-specific care

**Board minutes are public.** A static website can't hide pages behind a members-only
login; anyone can read them. Before posting, confirm the board has **approved this
version for public release**. If the full minutes shouldn't be public, offer to post
an approved summary instead. Remove personal phone numbers, home addresses, and
private personnel or financial details about individuals.

**Newsletters** often arrive as pasted email. Strip email-only bits (unsubscribe
links, "view in browser", tracking links, personal greetings like "Hi Jane") and keep
the substance. Keep past issues listed by month.

**Events**: include date, time, time zone if relevant, location (or "online"), cost,
and how to register. Ask whether past events should stay as an archive or be removed
afterwards; offer to remind them to tidy up after the date.

**People in photos and stories**: if a post names or shows children, clients, or
people the charity serves, check they have permission. Use first names only for
minors.

**Status claims**: don't write "tax-deductible" or "501(c)(3)" unless the charity is
IRS-recognized (see edit-my-site).

## 4. Publish

Run the **edit-my-site** loop: branch, plain-language preview (show the post as it
will read), pull request, checks, explicit yes, merge, then give them the direct
link to the new post once it's live.

Optionally, offer a short version of the post they could share on the charity's
Facebook and LinkedIn Pages, linking back to the site.
