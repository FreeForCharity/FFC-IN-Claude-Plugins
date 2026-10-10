# Setting up your own website-editing environment

For site owners whose website repository FFC has already created. The end state:
**you describe a change in plain English, Claude makes it, you approve it, and it
goes live.** No code editor, no command line, nothing to install besides Claude.

The full public walkthrough is https://ffcadmin.org/site-owner/ — this is the same
path, done together.

## Words they'll see (explain only when needed)

- **Repository ("repo")** — the folder holding your website's files. FFC made one
  just for your charity, usually named `FFC-EX-yourdomain.org`.
- **Branch** — a safe scratch copy where a change is drafted before going live.
- **Pull request ("PR")** — the "here's what changed — okay to publish?" page.
- **Merge** — saying "yes, publish this."
- **Checks** — automatic tests that confirm the site still builds. Green = safe.

## Steps, in order

### 1. GitHub account with MFA
Their own free account, in their real name, using an email they actually check
(the invitation arrives there). Turn on two-factor authentication with an
authenticator app. Guides: `github-account`, `multi-factor-authentication`.
Have them note their **username** exactly.

### 2. Ask FFC for access
FFC must add them to the charity's repository as a **writer**. Help them send
something like:

> Hi — this is <name> from <charity>. Please add my GitHub username <username> as a
> writer on our website repository so I can edit our site. Thank you!

Current contact details are on https://ffcadmin.org/site-owner/. Expect the
invitation within a day or so.

### 3. Accept the invitation
This is where most people get stuck. The invitation:
- arrives as an email from GitHub (check spam/promotions) **and** in GitHub
  notifications (the bell icon at github.com, signed in);
- can be accepted directly at
  `https://github.com/FreeForCharity/<repository-name>/invitations` while signed in;
- **expires after 7 days** — if it has, ask FFC to resend.

If they accept but still can't see the repository, they're almost always signed in
to a different GitHub account than the one FFC invited. Every-click walkthrough:
https://ffcadmin.org/site-owner/accept-invitation/

### 4. Install Claude
Claude Desktop on the computer and Claude on the phone: https://claude.ai/download.
FFC recommends the **Claude Pro** plan for ongoing work (the free plan is limited
and the GitHub connection is central to editing). Sign in.

### 5. Connect Claude to GitHub (once)
In Claude, connectors are added from the **+** button in the chat box or under
**Settings → Connectors**. Add **GitHub** and approve the sign-in in the browser
window that opens. Connector screens change over time; if what they see doesn't
match, follow what's on screen rather than insisting on exact menu names.

Connectors added on claude.ai or Desktop sync to the phone app automatically.

They should **never paste a token or password** into chat to make this work — the
connector sign-in is the right way.

If the tools/connector icon doesn't appear afterwards, fully quit Claude Desktop
(not just close the window) and reopen it.

### 6. Confirm it works
Ask them for their repository address (e.g. `github.com/FreeForCharity/FFC-EX-yourcharity.org`)
and check you can see it. Tell them, in plain language, what website is inside it.
**That's the finish line for setup.**

### 7. First edit
Hand off to the **edit-my-site** skill for something tiny and safe — fixing a typo
or confirming the phone number. Doing one full loop (describe → read → approve →
live) is what builds confidence.

## Optional, only when FFC asks

- **Cloudflare:** if FFC invites them, create a personal free account
  (guide: `cloudflare-account`), turn on 2FA, and accept the invite. **Never add the
  domain or website to their own account** — FFC manages it.
- **Charity email (Microsoft 365):** after the domain exists, first sign-in and MFA
  (guide: `microsoft-365-email`).
- **Website analytics:** `google-analytics`, `microsoft-clarity`,
  `google-search-console` — FFC places any DNS records; the owner never edits DNS.

## Going further (not required)

People who want to work like FFC developers — VS Code, Claude Code, running the site
locally — can read https://ffcadmin.org/developer-environment-setup/. Most site owners
never need it.
