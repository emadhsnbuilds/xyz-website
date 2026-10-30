# Context

Read this first in every new chat or Claude Code session.

## What we're building
A website for artxyz: we sell art products to customers living in Germany. What sets us apart: every product is made by people living in poverty.
(Sample content in this kit is for Linden & Hart, a brand strategy practice for small companies. Replace it with ours.)

## Our Git
- Design system: github.com/emadhsnbuilds/xyz-design-system
  Tokens (`assets/tokens.css`), components (`assets/components.css`), the storybook (`storybook.html`), the design skill (`SKILL.md`), and page designs in `prototypes/`.
- Website: github.com/emadhsnbuilds/xyz-website
  The pages Claude Code builds. `main` is the live site, `staging` is the rehearsal, every change goes through a pull request.
- The design system repository is the source of truth. The website only uses what is in it.

## Stack
Plain HTML, CSS and a little JavaScript. No build step. Hosted on Netlify, connected to the website repository. The contact form uses Netlify Forms.

## Pages
`index.html` (home) · `shop.html` · `about.html` · `contact.html` · `thanks.html` (after the form)

## How we work: the loop
1. Design in Claude chat: prototype the page, try versions, check phone and desktop.
2. Update the design system: anything reused or a rule goes into tokens, components, storybook and SKILL.md. The page goes into `prototypes/`.
3. Push the design system repository to GitHub.
4. Claude Code, in the website repository: get the latest design system, update tokens and components to match, build the page from its prototype, on a new branch.
5. Test on localhost: phone and desktop, every link, Lighthouse. Not OK? The report goes back to Claude chat.
6. Pull request, check the Netlify preview link, merge. The site goes live.

## Rules for Claude Code
- Never make a design decision. Colours, fonts, spacing, layout, copy, motion and imagery are decided in Claude chat and live in the design system or the prototype.
- If something isn't defined there, stop and ask. Offer two or three options with a short reason for each. Don't pick one yourself.
- Use only tokens from `assets/tokens.css` and components from `assets/components.css`. Never hard-code a value.
- Work on a branch, never directly on `main`.
- After building, run the site locally, test phone and desktop, and report what you built, what you tested and every open question, before opening a pull request.

## Current state
- Design system: Paper (editorial and calm), built from the Paper starter kit, with pictures (`media`) added for the home page.
- Both repositories are on GitHub. The design system repository holds the Paper kit and the home prototype (`prototypes/home.html`). The website repository has `assets/`, `netlify.toml` and `CLAUDE.md` on `main`; the home page (`index.html`) is on the branch `build/home`, in a pull request.
- Business name: artxyz.
- Still to decide in chat: the Shop, About and Contact pages and their copy (the home page links to `shop.html`, `about.html` and `contact.html`, which do not exist yet), the real pictures (the home prototype uses sample photos), and the makers' story.
