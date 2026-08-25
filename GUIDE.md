# Managing your Beyond the Baobab website

A plain-English guide to owning, changing, and publishing your site — with Claude Code (your AI "coworker") doing the technical parts for you. No coding required. You do not need to memorise any commands; you can always just **ask Claude in your own words**. This guide explains what's happening so nothing feels like a black box.

---

## What you've got

Your site is a single, self-contained folder. There is **no database and no build step** — it's just files a browser can open.

```
beyond-the-baobab/
├── index.html      ← the entire website (text, layout, and behaviour)
├── assets/         ← all the images and videos
└── GUIDE.md        ← this guide
```

To see the site right now, **double-click `index.html`** — it opens in your web browser.

---

## Part 1 — One-time setup (about 20 minutes)

You only ever do this once.

### 1. Install the tools

- **Claude Code** — your AI coworker that edits the site and handles GitHub for you. Install it from **https://claude.com/claude-code** and sign in.
- **A GitHub account** — free cloud storage + backup for your site. Sign up at **https://github.com/signup**. Pick a username you're happy to keep (e.g. `beyondthebaobab`).
- **Git** — the tool that saves versions of your site. It's already on most Macs. On Windows, Claude will point you to it if it's missing.

### 2. Put the site on your computer

You were sent a **ZIP file**. Unzip it somewhere you'll remember, e.g. `Documents/beyond-the-baobab`.

### 3. Open the folder in Claude Code

Open Claude Code and point it at that folder (open the folder from the app, or in a Terminal type `cd` then drag the folder in, press Enter, and run `claude`). From now on, you just **type what you want in plain English.**

### 4. Put your site on GitHub (let Claude do it)

In Claude Code, type something like:

> **"Create a new private GitHub repository called beyond-the-baobab and push this whole folder to it."**

Claude will do it. The first time, it may ask you to log in to GitHub — it'll tell you to run `gh auth login`. Just type `!gh auth login` into Claude and follow the browser prompts (choose **HTTPS** and **Login with a web browser** if asked). Then ask Claude to try again.

That's it — your site is now safely backed up in the cloud, and every future change is saved with it.

---

## Part 2 — Getting a live web link (publishing)

Two easy ways. Ask Claude to walk you through whichever you prefer.

- **Easiest — Netlify Drop:** go to **https://app.netlify.com/drop** and drag your site folder onto the page. You get a live link in seconds. To update it later, drag the folder again.
- **With GitHub — GitHub Pages (free):** once your site is on GitHub (Part 1), ask Claude:
  > "Turn on GitHub Pages for this repo so the site is live."

  Your site goes live at `https://your-username.github.io/beyond-the-baobab/`. After this, **every time you push a change (see Part 4), the live site updates automatically.**

When you're ready to use your real web address (e.g. `beyondthebaobab.com`), ask Claude: *"How do I point my domain at this site?"*

---

## Part 3 — Changing the site with Claude

This is the everyday loop:

1. **Ask** Claude for a change, in plain English.
2. Claude **edits** the files.
3. **Look** at it — reload `index.html` in your browser (or say *"open the site"*).
4. If you like it, **save and publish** it (Part 4). If not, say *"undo that"* or ask for a tweak.

### Examples of good prompts

- *"Change the hero headline to 'Botswana, the way we'd travel it'."*
- *"Add a new FAQ. Question: 'Do you arrange honeymoons?' Answer: 'Yes — …'."*
- *"Replace the founder photo. I've saved the new one on my Desktop as `kristy.jpg`."*
- *"Update the July sample-trip price to £9,200."*
- *"The partner logos feel too big on my phone — make them a bit smaller on mobile."*
- *"Change the enquiry email address to hello@beyondthebaobab.com everywhere."*

### Tips for getting what you want

- **Point at the section** ("in the testimonials…", "the map section…"). Claude knows the page well, but naming the spot helps.
- **One change at a time**, then look at it. Easier to see what happened.
- **Ask to preview before saving**: *"show me before we save it."*
- **Be specific with words** — for text changes, give the exact wording you want.
- **You can't really break anything.** Every saved version is kept; you can always go back (see below).

### Hiding and bringing back sections

Any part of the page — a whole section, a single card, the map — can be **switched off without deleting it**, and switched back on later exactly as it was. Nothing is lost, so you can toggle sections on and off freely as your content changes with the seasons.

- *"Hide the Field notes section for now."*
- *"Bring the Field notes section back."*

If you'd rather remove something for good, say *"delete the … section"* — and even that can be undone afterwards if you change your mind.

---

## Part 4 — Git in plain English (commit & push)

Git is just **version history + cloud backup**. Two words to know:

- **Commit** = *save a snapshot, with a short note.* Like hitting Save, but it also labels the moment (e.g. "update July price") so you can find it later.
- **Push** = *upload your saved snapshots to GitHub* (the cloud). This backs them up — and, if you're using GitHub Pages, **publishes them to your live site.**

You don't have to type git commands. After a change you're happy with, just say:

> **"Commit this and push it."**

Claude writes a sensible note, saves the snapshot, and uploads it. Done.

Other things you can just ask for:

| You want to… | Say to Claude |
|---|---|
| Save + publish a change | "Commit this and push it." |
| Undo the last change | "Undo your last change." |
| Go back to how it was earlier | "Roll the site back to yesterday's version." |
| See what's changed | "What's changed since the last save?" |
| Back up without publishing | "Commit this but don't push yet." |

**Rule of thumb:** commit when a change is finished and you like it; push to back it up (and go live).

---

## Part 5 — Before you promote the site widely

A short to-do list of things that are placeholders or worth double-checking. Ask Claude to help with any of them.

- **Enquiry form:** right now, "Send enquiry" opens the visitor's own email app with the details filled in. That works, but it depends on them having email set up. For enquiries to land straight in your inbox, ask Claude: *"Wire the enquiry form up to Formspree"* (a free service — you'll paste in one code it gives you).
- **Testimonials:** the quotes and names are real — just double-check the country and trip label under each name is correct, and add guest photos if you have them.
- **Prices:** check the three sample-trip prices and the budget bands in the enquiry form are accurate.
- **Field notes:** the three article cards at the bottom don't link anywhere yet. Either add real articles, or ask Claude: *"Hide the Field notes section until we have articles."*
- **Contact details:** confirm the email and phone number in the enquiry section and footer are correct.

---

## Part 6 — Building changes safely (without breaking the live site)

**The golden rule: the version people can see should always be one you trust. Do your experimenting on a copy — never on the live site.**

Git gives you a clean way to do this with **branches**. Think of a branch as a parallel copy of the site inside the same project, where you can try anything freely. Your live site stays on the **`main`** branch; you tinker on a branch; and only when you're happy do you fold the changes back into `main`.

### The safe loop

1. **Start a branch** — *"Create a branch called homepage-refresh and switch to it."*
2. **Make your changes** and preview them in the browser. The live site is untouched this whole time.
3. **Happy with it?** — *"Merge homepage-refresh into main and push."* Now it's live.
4. **Didn't work out?** — *"Throw away this branch, I don't want these changes."* The live site never saw them.

### Building a bigger "version 2"

For a larger redesign you'll work on over days or weeks, the same idea scales:

- Keep the current site live on `main`.
- *"Create a branch called v2 and let's rebuild the homepage there."*
- Build it up over time, previewing as you go — `main` (your live site) stays safe and unchanged.
- When v2 is ready: *"Merge v2 into main and publish."*

### Even simpler (no git at all)

If branches feel like a lot at first, the low-tech version is fine: **duplicate the whole folder** (e.g. `beyond-the-baobab-v2`), experiment in the copy, and publish the copy when you're happy. You lose the tidy history, but your live site is safe.

### A few good habits

- **Commit often, in small steps.** Each commit is a checkpoint you can return to — ten small saves beat one giant one.
- **Preview before you publish.** Always look at a change in the browser before merging or pushing.
- **`main` is sacred.** Treat whatever's on `main` as "what the world sees." Only put tested, working changes there.
- **GitHub is your safety net.** Every version is saved there, so you can always go back. You cannot truly lose the site.
- **When in doubt, ask.** *"Is it safe to publish this?"* or *"What will this change affect?"* — Claude will tell you before you commit to anything.

---

## If something looks wrong

- Made a change you don't like? → *"Undo your last change."*
- Site looks broken? → *"The site looks broken after that last change — can you fix or undo it?"*
- Not sure what something does? → just ask Claude to explain it.

You're in good hands — take your time, change one thing, look at it, and save when you're happy. Everything is reversible.

---

*Designed by Our Social Creative.*
