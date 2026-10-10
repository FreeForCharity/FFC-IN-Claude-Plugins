---
name: check-my-site
description: Reviews a Free For Charity (FFC) charity website and gives its owner a plain-language health report — does it load, is the FFC footer complete and accurate, are contact details consistent, are links and images working, is anything out of date, is it readable on phones and accessible — then offers to fix what the owner can fix and drafts a note to FFC for what only FFC can fix. Use this whenever someone asks if their charity's site is working, looks right, is up to date, is ready for review or approval, why something looks broken, or wants a check-up before an event, grant application, or board meeting.
---

# Check My Site

Give the owner a clear, honest picture of their website's health, in plain
language, and a short list of what to do about it. They should finish knowing
what's fine, what needs attention, and who fixes it.

## 1. Get the address

Ask for their site's address if you don't know it. It will be either their own
domain (e.g. `https://yourcharity.org`) or, before the domain is connected, the
preview address `https://freeforcharity.github.io/FFC-EX-<domain>/`. If you have the
GitHub connector and access to their repository, use both: the live pages show what
visitors see, and the repo shows why.

## 2. Check

Fetch the home page and each page linked from the main navigation and footer. Look
at:

**Basics**
- Each page loads (no error page, no "page not found")
- Images appear (no broken image references)
- Links work — especially Donate, Contact, and social links

**FFC footer** (part of every FFC site, required by the Terms of Service)
- Organization's legal name and EIN are present and match what they expect
- Policy links work: privacy policy, terms, accessibility / cookie information
- Social links point to the organization's Pages
- Credit to Free For Charity is present
- **Status wording matches reality:** a **501(c)(3)** site may show the 501(c)(3)
  status line and a Candid/GuideStar link; a **pre-501(c)(3)** site must **not** claim
  501(c)(3) or tax-deductible status. Ask which they are if you can't tell.

**Accuracy and freshness**
- Phone, email, and address are the same everywhere
- Past events still advertised as upcoming; "latest news" that's very old; last
  year's dates
- Placeholder or template text left over (e.g. "Lorem ipsum", "Your Charity Name",
  example phone numbers)

**Phones and accessibility** — what you can tell from the page source
- A mobile viewport tag is present
- Images have meaningful alt text
- Headings are in a sensible order; link text says where it goes (not "click here")

**Repository** (only if you have GitHub access)
- The latest run of the checks on `main` passed
- Any open pull requests they may have forgotten to approve

## 3. Be honest about limits

From a chat you can't fully test how the site behaves in a browser — real phone
layout, browser console errors, or a full accessibility score. Say so, and give them
a 1-minute manual check: open the site on their phone, scroll every page, tap the
menu, the Donate button, and the phone number. Don't report anything as "passed"
that you didn't actually check.

## 4. Report

Use this shape, in plain words:

```
Your site: <address> — checked <date>

✅ Working well
- ...

⚠️ Worth fixing (you can do these with me)
- <problem> — <why it matters, one line> — <offer: "Want me to fix it?">

❌ Needs FFC
- <problem> — <why only FFC can fix it>

📱 Quick check for you to do on your phone
- ...
```

Keep it short: lead with what matters most to visitors (can people donate and
contact you?). If everything's fine, say so plainly — a clean report is good news.

## 5. Next steps

- Things the owner can fix (content, contact info, old events, alt text) → offer to
  do them now with the **edit-my-site** skill, one at a time.
- Domain not working, security certificate warnings, email, footer data that comes
  from their FFC application, or failed checks you can't resolve → draft a message
  with the **ask-ffc-for-help** skill.
