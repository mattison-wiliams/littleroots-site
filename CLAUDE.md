# Little Roots School website

Simple static HTML/CSS site hosted on Netlify. Netlify publishes whatever is on the `main` branch.

## Working with the site owner

- The owner is not a developer. Explain what changed in plain, friendly English, with no code or jargon.
- When asked to make a change, just make it. When done, summarize what changed, then save it (commit and push to the working branch) without publishing.

## Publishing (Netlify credits)

- Every push to `main` is a Netlify production deploy, and each one uses credits from a limited monthly allowance. In September 2026 the credits ran out from publishing after every small edit.
- Do not push to `main` after each change. Save changes on the working branch and publish only when the owner says "publish" (or clearly asks for it to go live). Then publish everything in one push to `main`.
- After each change, remind the owner in one short line that it's saved but not live yet, and to say "publish" when they're ready.
- Changes that don't affect the website itself (like edits to this file or the redesign notes) can go to `main` with `[skip netlify]` in the commit message, so Netlify doesn't build or use credits.
- Keep it simple. Do not add frameworks, build tools, or dependencies.

## Writing style for site text

- Do not use dashes (-, –, —) or semicolons in visible text. Use commas, colons, periods, or "to" for ranges.
  - Exceptions the owner chose to keep: the class time "9:30–11:00 AM" in the footer, and product names that include a dash on the Recommended Gear page.
- Words for the adult who comes to class: use "you" when talking to the parent reading the page, "parent or caregiver" for rules (like who has to stay), and "parents and caregivers" in search and link preview descriptions. "Grown-ups" (with the hyphen) is allowed in playful spots, like the question of the day.
- Use "a month" for prices (for example "$99 a month"), not "/month" or "per month".
- Ages are written "ages 1 to 3".
- Pricing is $99 a month. The only term pass offered right now is Winter (December 2, 2026 to February 24, 2027): $229, nonrefundable, sibling $109. Siblings are otherwise $49 a month. Spring, Summer, and Fall passes are $269 (sibling $129). Their dates and prices are listed on the Register page for planning, but only the Winter pass has a payment button for now. There is no longer any bundle.
- Refer to the owner's child as "my daughter" on the site, not by name.
- Parent testimonials are quoted word for word. Do not edit or flag their wording.
- The header name is "Little Roots School" on purpose, ahead of a planned preschool rebrand. Do not flag it as inconsistent with "Little Roots Forest School" elsewhere.

## Homepage hero line

- The line under "Kids being kids in the forest." changes each season. It pairs one real moment from the trail with one real messy moment from the stations, taken from that season's lesson plans. Avoid lists of three.
- Current (fall 2026): turning over logs to see who lives underneath, and leaf soup in the mud kitchen. Swap for winter when the Winter term starts December 2.

## Photos

- Always strip hidden photo data (location, date, phone model) before adding a photo to the site.
- Resize and compress photos so pages stay fast, and save them as .jpg in the `images` folder with simple lowercase names.
- Write a short, descriptive alt text for every photo.
- Check how the photo is cropped on both phone and computer screen sizes.

## Before publishing

- Preview changed pages at phone and computer widths and make sure nothing scrolls sideways on phones.
