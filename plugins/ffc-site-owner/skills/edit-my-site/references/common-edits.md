# Common edits — what to watch for

The everyday changes site owners ask for (mirrors
https://ffcadmin.org/site-owner/common-edits/), with the details that are easy to
miss.

## Contact info (phone, email, address)
- Search the **whole repo** for the old value — header, footer, contact page, data
  files, and any structured data/JSON-LD in the layout. Update every occurrence.
- Keep the existing format (e.g. `(520) 555-1234` vs `520-555-1234`) consistent.
- Phone links use `tel:+1XXXXXXXXXX`; email links use `mailto:`. Update both the
  visible text and the link.
- The **footer's** organization details may be generated from the charity's FFC
  application data. If the contact info is in the footer and you can't find it as
  plain text in the repo, it's coming from that data — route to FFC.

## Hours / service times
- Update every place they appear; keep one consistent format.
- For a **temporary** change (holiday closure), ask when it should be removed and
  remind them to come back to undo it — or suggest wording that dates itself
  ("Closed Monday, May 25 for Memorial Day").

## Donate link or button
- Confirm the new link is the charity's own donation page (e.g. its Zeffy form) and
  starts with `https://`.
- Check every donate button/link, not just the first one found.
- Never put payment details or bank information on the site.

## Logo or photo
- Ask for the image file if they haven't attached it.
- Replace the file *or* update references — don't leave the old file referenced
  anywhere. Logos may also be used for the favicon and social-sharing image
  (`og-image`); mention this and ask whether they want those updated too.
- New alt text that describes the image (logo alt = the organization's name).

## Edit a section of text
- Keep their wording; fix only obvious typos unless they ask for polishing.
- Preserve headings and structure so the page layout doesn't shift.

## Add or update a team / board member
- Copy the shape of an existing entry exactly (name, role, bio, photo, order).
- Ask whether the person has agreed to be listed publicly with that photo and bio.
- For removals, ask whether to remove entirely or move to a "past" list if the site
  has one.

## Social media links
- Use the organization **Page** URLs, not anyone's personal profile.
- Remove dead platforms rather than leaving broken links.
- Social links may also live in the footer data — check both.

## Colors / brand accents
- Check text contrast against the new color meets WCAG AA (4.5:1 for normal text,
  3:1 for large text). If it doesn't, explain and suggest the closest accessible
  shade.
- Find where the theme color is defined (often CSS variables in
  `src/app/globals.css`) and change it there, not per-component.

## Add a new page
- Kebab-case route folder, add it to navigation and sitemap the way existing pages
  are, and give it a clear title and description.
- A new FFC site often starts as a single page and grows; ask whether this should be
  a new section on the home page instead.
