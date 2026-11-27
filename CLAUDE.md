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

- Do not use dashes (– or —) to break up sentences, or semicolons, in visible text. Use commas, colons, periods, or "to" for ranges. Hyphens in normal hyphenated words are fine (like "hands-on" or "Washington-licensed").
  - Exceptions the owner chose to keep: the class time "9:30–11:00 AM" in the footer, and product names that include a dash on the Gear Guide page.
  - The dash the owner dislikes is the em dash (—). A plain hyphen like "K-8" is fine. Do not flag "K-8" or treat it as a dash problem.
- Words for the adult who comes to class: use "you" when talking to the parent reading the page, "parent or caregiver" for rules (like who has to stay), and "parents and caregivers" in search and link preview descriptions. "Grown-ups" (with the hyphen) is allowed in playful spots, like the question of the day.
- November 2026: the owner chose to remove the prorated example prices ($74, $49) from the Enroll page and FAQ. The site just says the first month is prorated and she emails the exact amount. Do not add the examples back. A full December 2026 is $74 (three classes, break December 23 and 30), shown in the December box on the Enroll page. Families who start partway through any month pay $24 for each class left. The owner does not want specific partial-month examples on the site.
- November 20, 2026: almost every family starts with a trial, so the Enroll page order is: intro, "Start With a Trial Class", "Choose How to Pay", then "Ready to Enroll?" (just the enrollment form button, no pay step. How to pay is in the Monthly and Winter cards). The top of the page says when and where class meets and that a parent or caregiver stays.
- Prorating math, for reference (updated November 20, 2026 by the owner): $24 for each class left in the first month, up to $74. One left is $24, two left is $48, three or more left is $74. The older $49 figure for two classes is no longer used.
- November 20, 2026: the owner said that after a $15 trial class, the rest of that month is "$24 for each class left, up to $74." This wording is in the "Start With a Trial Class" section of the Enroll page and the FAQ trial answer. The $15 trial does not count toward tuition.
- November 22, 2026: the homepage tuition box has a line under the price: "December is $74 because we have three classes. See why" (links to the December box on the Enroll page). Remove it in early January 2027, when monthly is back to $99.
- Monthly tuition bills on the 1st of each month.
- Babies under 12 months: $49 a month when joining on their own, free with a paid sibling (FAQ).
- Use "a month" for prices (for example "$99 a month"), not "/month" or "per month".
- Ages are written "ages 1 to 3".
- Grade ranges are written "K to 8" (also "K to 5", "K to 3", and so on) to stay consistent across the site, even though "K-8" isn't against the style rules.
- Pricing is $99 a month. The only term pass offered right now is Winter (December 2, 2026 to February 24, 2027): $229, nonrefundable, sibling $109. Siblings are otherwise $49 a month. Older siblings tag along free, or pay the $49 sibling price if they join in fully with their own materials. Spring, Summer, and Fall passes are $269 (sibling $129). Their dates and prices are listed on the Register page for planning, but only the Winter pass has a payment button for now. There is no longer any bundle. Monthly families who switch to the Winter pass pay for it on the Enroll page, and their monthly tuition is paused December through February. November 27, 2026: the owner had the "by November 27" deadline removed from the FAQ. Do not add it back. Winter pass families who sign up by Friday, November 20 get a winter play kit (moved from November 18), handed out at Gratitude morning on November 25. The Winter savings is $43 (monthly for winter is $272: $74 for December with three classes, then $99 for January and February). November 20, 2026: the owner removed the free November 25 class for new Winter pass families (new families can use the $15 trial for that class) and the "December 2 last day for new families" line. Do not add these back. The Winter pass stays up until monthly becomes the better deal, then it switches to the Spring pass. The Enroll page Winter card is kept short (dates, $272 monthly comparison, pay first, then new families fill out the enrollment form. The owner wants Winter pass families to pay before the form so they commit right away, siblings $109) and links to the FAQ term pass answer (faq.html#term-passes) for switching from monthly and other details. The play kit line is on the card only through November 20, 2026. Remove it on November 21.
- Refer to the owner's child as "my daughter" on the site, not by name.
- Parent testimonials are quoted word for word. Do not edit or flag their wording.
- Do not mention the preschool plans anywhere on the site. They are not public yet.
- The header name is "Little Roots School" on purpose, ahead of a planned preschool rebrand. Do not flag it as inconsistent with "Little Roots Forest School" elsewhere.

## Writing tells to avoid

The owner dislikes these AI writing habits. Avoid them in site text and in anything written for the owner (emails, captions, drafts).

- "That's the point." and any "that's the..." phrasing
- "It's not X, it's Y."
- "More than just..."
- "At the heart of..."
- "A place where..."
- "Whether you're..."
- "That's where..."
- "Here, we..."
- "We don't ___, we ___."
- Too many lists of three
- Strings of short, punchy sentences
- Polished brand manifesto language
- Fake emotional conclusions
- Neat rhetorical reversals and overly symmetrical sentences
- Made up sayings or clever closing lines
- Generic words: "intentional," "meaningful," "thoughtfully curated," "foster," "cultivate," "empower," "nurture"
- Em dashes

Exception the owner chose to keep: "That's where my love of early childhood first took root" in the About page story. Do not flag it.

## Homepage hero line

- The line under "Kids being kids in the forest." changes each season. It pairs one real moment from the trail with one real messy moment from the stations, taken from that season's lesson plans. Avoid lists of three.
- Current (fall 2026, written by the owner for mushroom week): "This fall we're watching the forest change, from the first yellow leaves to the mushrooms that come up after the rain." On November 19 the owner tried a late fall version ("This time of year we're bundled up and stomping through puddles...") but chose to hold off. She likes the puddles part. A new line should keep it and pair it with a real stations moment she gives. Do not swap it without her.

## Photos

- Always strip hidden photo data (location, date, phone model) before adding a photo to the site.
- Resize and compress photos so pages stay fast, and save them as .jpg in the `images` folder with simple lowercase names.
- Write a short, descriptive alt text for every photo.
- Check how the photo is cropped on both phone and computer screen sizes.
- Do not re-compress the existing banner photos to make pages faster. It was tried and made them blurry.

## Dates that go stale

- Weeks that have passed come out of the themes lists on the Home, Enroll, and Stations pages. On November 27, 2026 the owner had the November 25 lines removed there and from the FAQ and Stations text. The question on Home and Enroll now reads "What are the themes in December?", so rename it when the month changes.
- The homepage "December is $74" line comes out in early January 2027 (see the November 22 note above).
- The FAQ entry "What are the important dates for 2026 to 2027?" needs the new year's dates when the next calendar comes out.

## Accessibility

- November 27, 2026: added an Accessibility page (`accessibility.html`). It is linked at the end of the footer link row on every page, so any new page needs that footer link too, plus the "Skip to main content" link and one `<h1>`.
- The page makes promises to visitors, so keep them true: photos have alt text, every page has the skip link and headings in order (no skipped levels), links that open a new tab have the hidden "(opens in new tab)" note (`<span class="sr-only">`), the menus and buttons work with a keyboard, and nothing scrolls sideways on phones.
- The page also says the sign-up forms are made by Jotform and that anyone who has trouble with a form can email, and the owner will email them the form to fill out (that is how she registers them in that case). It also says the 2026 to 2027 calendar PDF may not read well in a screen reader. The calendar PDF is not set up for screen readers (the family handbook is). The FAQ entry "What are the important dates for 2026 to 2027?" (`#important-dates`) is the plain text version of the calendar's Key Dates, so keep it in sync when dates change and update it each school year. If the calendar is remade as a tagged PDF, update that line on the Accessibility page.
- November 27, 2026: the owner confirmed that all three Jotform forms linked from the site (trial booking, enrollment, email list) show Jotform's "Accessibility Enabled Form" badge, and the Accessibility page says the setting is on for all of them. Any new Jotform form linked from the site needs Jotform's Form Accessibility setting turned on (with the badge shown) and should be run through Jotform's built-in accessibility check, or that statement stops being true. The liability waiver families sign by email is a separate Jotform Sign document ("Little Roots Waiver") and was not part of that check.
- When a link's words are vague or repeated but it goes somewhere different (like "try your first class for $15" that goes to the Enroll page instead of the booking form), add hidden screen reader text with `<span class="sr-only">` instead of changing the visible words.
- Do not flag the repeated "Enroll" links. They all go to the same page, which is fine. Do not flag the round arrow at the bottom right of long pages as an empty "#" link. It is the "Back to top" button, it has a name, and it stays hidden until you scroll.
- For sage-green text on the cream background use `--sage-text`, not `--sage`. `--sage` is too pale to read (about 3 to 1).
- The FAQ search box has a darker green outline on purpose (the old pale one was hard to see).
- November 27, 2026: the owner approved a lighter touch on the banners. The green panel on the homepage hero, the dark gradients on the Approach, Stations, FAQ, and Enroll banners (computer size), and the "No experience needed" band were darkened a little, so all 76 spots where words sit on a photo pass the strict contrast check (before, about 20 fell short). When a banner photo or its gradient changes, check that the words still stand out, especially the small italic line under each title and the phone sizes. Ask the owner before darkening more.
- The calendar PDF circles Thursday, September 3, 2026 as the first class day, while every other class day is a Wednesday. It is probably a typo, so fix it the next time the PDF is remade.
- How the site was checked: the free axe-core checker run in a headless browser against every page at phone (390 px) and computer (1280 px) widths, from a scratch folder outside the project (never add it to the site). Text over photos needs its own check: hide the words and measure the pixels behind them.

## Before publishing

- Preview changed pages at phone and computer widths and make sure nothing scrolls sideways on phones.

## Tutoring page facts

- "5 years in public schools" is correct. It counts student teaching along with Centennial (2 years), subbing (1 year), and math intervention (1 year). Do not flag it as adding up to 4.
- The owner chose to keep "About me" where it is on the tutoring page (right after "What I tutor"). Do not suggest moving it lower.
- "What I tutor" uses one combined "K to 8" subject list on purpose, not separate elementary and middle school lines, because some middle schoolers still need phonics and reading support. Do not split it by grade.
- Example goals are split by readiness ("I can" goals, then SMART goals when the child is ready), not by grade. Do not add grade ranges back to them.
- "Sprocket" is a real science curriculum (from NCEE) the owner taught at Centennial. It is not a typo.
- The preschool line says "For three years" on purpose instead of years, because the owner left the preschool in winter and the Golden Apple came the next fall. Do not flag a timeline overlap.
