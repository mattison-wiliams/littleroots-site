# Little Roots Gear Page Redesign — Claude Code Handoff

This document describes three separate changes to `recommended/index.html` and `css/style.css`.
Make each change separately and test on mobile (375px) before moving to the next.
**Do not touch the banner or any existing copy or affiliate links.**

---

## Change 1: Add hero CSS

**Why:** The hero HTML is already in place but the CSS rules that make it work (full-bleed photo, overlay, cream text) are missing from `style.css`.

**What to do in `css/style.css`:**

Add after the existing `.hero` styles:

```css
/* ===== Gear Page: Hero ===== */
.gear-hero {
  position: relative;
  overflow: hidden;
  min-height: 440px;
  display: flex;
  align-items: flex-end;
  padding: 0;
}

.gear-hero-img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 35%;
  z-index: 0;
}

.gear-hero-overlay {
  position: absolute;
  inset: 0;
  z-index: 1;
  background: linear-gradient(
    to bottom,
    rgba(0,0,0,.08) 0%,
    rgba(0,0,0,.02) 35%,
    rgba(0,0,0,.58) 100%
  );
}

.gear-hero .container {
  position: relative;
  z-index: 2;
  padding-top: 3rem;
  padding-bottom: 3rem;
}

.gear-hero h1 {
  color: var(--cream);
  font-size: 4rem;
  margin-bottom: 10px;
}

.gear-hero .subtitle {
  color: rgba(255,249,240,.88);
  font-style: italic;
  font-size: 1.1rem;
  max-width: 480px;
  margin: 0;
}
```

Add inside the existing `@media (max-width: 768px)` block:

```css
  .gear-hero {
    min-height: 340px;
  }

  .gear-hero h1 {
    font-size: 2.8rem;
  }
```

**No changes to `recommended/index.html` for this step** — the HTML is already correct.

---

## Change 2: Quick-nav, partner cards, section headers, affiliate note

**Why:** Four polish items that make the page feel more intentional and easier to navigate.

### 2a — Quick-nav

**What to do in `recommended/index.html`:**

Directly after the closing `</section>` tag of the hero, add:

```html
<nav class="gear-quicknav" aria-label="Jump to section">
  <div class="container gear-quicknav-inner">
    <a href="#the-backpack">The Backpack</a>
    <a href="#summer">Summer</a>
    <a href="#fall-winter-spring">Fall, Winter &amp; Spring</a>
    <a href="#year-round">Year-Round</a>
  </div>
</nav>
```

Also add `id` attributes to the four main sections so the links work:

- Add `id="the-backpack"` to the `<section>` wrapping The Backpack content
- Add `id="summer"` to the `<section>` wrapping Summer Gear
- Add `id="fall-winter-spring"` to the `<section>` wrapping Fall, Winter & Spring Gear
- Add `id="year-round"` to the `<section>` wrapping Year-Round Essentials

**What to do in `css/style.css`:**

```css
/* ===== Gear Page: Quick-nav ===== */
.gear-quicknav {
  position: sticky;
  top: 73px;
  z-index: 90;
  background-color: var(--cream);
  border-bottom: 1px solid rgba(122,154,109,.2);
}

.gear-quicknav-inner {
  display: flex;
  overflow-x: auto;
  scrollbar-width: none;
  -webkit-overflow-scrolling: touch;
}

.gear-quicknav-inner::-webkit-scrollbar {
  display: none;
}

.gear-quicknav-inner a {
  display: block;
  padding: 13px 20px;
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.03em;
  color: var(--warm-brown);
  text-decoration: none;
  white-space: nowrap;
  border-bottom: 2px solid transparent;
  transition: color 0.2s, border-color 0.2s;
}

.gear-quicknav-inner a:hover,
.gear-quicknav-inner a.active {
  color: var(--forest-green);
  border-bottom-color: var(--forest-green);
}
```

Add inside the existing `@media (max-width: 768px)` block:

```css
  .gear-quicknav {
    top: 65px;
  }
```

### 2b — Partner cards

**What to do in `recommended/index.html`:**

Remove the two existing Oaki and Reima `<section>` blocks:

```html
<!-- REMOVE these two sections entirely -->
<section class="section" style="padding-top: 0;">
  <div class="container">
    <div class="tip-callout" style="margin-top: 0;">
      <p>We love Oaki for rain gear ...</p>
    </div>
  </div>
</section>

<section class="section" style="padding-top: 0;">
  <div class="container">
    <div class="tip-callout" style="margin-top: 0;">
      <p>We also love Reima ...</p>
    </div>
  </div>
</section>
```

At the end of the intro `<section>`, inside `.container`, after the last `</p>` of `.recommended-intro`, add:

```html
<div class="gear-partners">
  <div class="gear-partner-card">
    <span class="gear-partner-name">OAKI</span>
    <p>Our go-to for rain suits, boots, and cold-weather gear. Little Roots families get <strong>25% off orders over $29.99</strong> plus free shipping over $100.</p>
    <span class="gear-partner-code">LITTLEROOTS</span>
  </div>
  <div class="gear-partner-card">
    <span class="gear-partner-name">Reima</span>
    <p>Finnish brand, PFAS-free since before it was a marketing angle. You&rsquo;ll find specific product links throughout the page, or shop their full collection:</p>
    <a href="https://www.awin1.com/cread.php?awinmid=92285&awinaffid=2853489&ued=https%3A%2F%2Fus.reima.com%2F%3Ff%3Dtrue" target="_blank" rel="noopener" class="gear-partner-link">Shop Reima &rarr;</a>
  </div>
</div>
```

**What to do in `css/style.css`:**

```css
/* ===== Gear Page: Partner Cards ===== */
.gear-partners {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  max-width: 720px;
  margin-top: 32px;
}

.gear-partner-card {
  background-color: var(--sage-light);
  border: 1px solid rgba(122,154,109,.25);
  border-radius: 12px;
  padding: 20px 22px;
}

.gear-partner-name {
  font-family: 'Caveat', cursive;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--forest-green);
  display: block;
  margin-bottom: 6px;
}

.gear-partner-card p {
  font-size: 0.88rem;
  line-height: 1.6;
  color: var(--warm-brown);
  margin-bottom: 12px;
}

.gear-partner-code {
  display: inline-block;
  background-color: var(--forest-green);
  color: var(--cream);
  font-family: 'Lora', Georgia, serif;
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  padding: 4px 12px;
  border-radius: 20px;
}

.gear-partner-link {
  font-size: 0.88rem;
  font-weight: 600;
  color: var(--forest-green);
  text-decoration: underline;
}
```

Add inside the existing `@media (max-width: 768px)` block:

```css
  .gear-partners {
    grid-template-columns: 1fr;
  }
```

### 2c — Section header treatment

**What to do in `recommended/index.html`:**

Replace each `<h2 class="section-title">` in the four main gear sections with this pattern:

```html
<!-- REPLACE -->
<h2 class="section-title">Summer Gear (June through September)</h2>

<!-- WITH -->
<div class="gear-section-label">
  <h2>Summer Gear</h2>
</div>
<p class="gear-section-season">June through September</p>
```

Do the same for the other three sections, using these labels:

- "The Backpack" (no season line)
- "Fall, Winter &amp; Spring Gear" / "October through May"
- "Year-Round Essentials" (no season line)

**What to do in `css/style.css`:**

```css
/* ===== Gear Page: Section Headers ===== */
.gear-section-label {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 8px;
}

.gear-section-label h2 {
  font-size: 2.2rem;
  margin: 0;
  white-space: nowrap;
}

.gear-section-label::after {
  content: '';
  flex: 1;
  height: 1px;
  background-color: rgba(122,154,109,.3);
}

.gear-section-season {
  font-size: 0.85rem;
  font-style: italic;
  color: var(--sage-text);
  margin-bottom: 20px;
}
```

### 2d — Affiliate note

**What to do in `recommended/index.html`:**

Remove the existing inline-styled paragraph at the bottom of `<main>`:

```html
<!-- REMOVE this -->
<p style="text-align: center; font-family: 'Lora', Georgia, serif; font-size: 0.78rem; color: #9a8070; max-width: 640px; margin: 0 auto 2rem; padding: 0 1.5rem;">Some links on this page are affiliate links. If you purchase through them, a small percentage supports Little Roots at no extra cost to you.</p>
```

Add this directly before `<footer class="site-footer">`:

```html
<div class="gear-affiliate-note">
  <p>Some links on this page are affiliate links. If you purchase through them, a small percentage supports Little Roots at no extra cost to you.</p>
</div>
```

**What to do in `css/style.css`:**

```css
/* ===== Gear Page: Affiliate Note ===== */
.gear-affiliate-note {
  text-align: center;
  padding: 20px 5%;
  background-color: var(--sage-light);
  border-top: 1px solid rgba(122,154,109,.2);
}

.gear-affiliate-note p {
  font-size: 0.8rem;
  color: var(--sage-text);
  font-style: italic;
  max-width: 560px;
  margin: 0 auto;
  line-height: 1.6;
}
```

---

## Change 3: Product block cleanup

**Why:** Product entries currently borrow `.belief-block` (an About page class). Giving them their own class keeps the stylesheet clean and product descriptions visually lighter.

**What to do in `recommended/index.html`:**

Replace every instance of `class="belief-block product-block"` with `class="gear-product"`:

```html
<!-- REPLACE every instance of -->
<div class="belief-block product-block">

<!-- WITH -->
<div class="gear-product">
```

There are approximately 20 instances across the page. Use find-and-replace.

Also remove every `<div class="faq-list">` wrapper div and its closing `</div>` — these are redundant wrappers around individual `<details>` elements that add no structure. Each `<details class="faq-item">` should sit directly inside the `.container`.

**What to do in `css/style.css`:**

Add after the existing `.product-block` styles:

```css
/* ===== Gear Page: Product Blocks ===== */
.gear-product {
  padding: 18px 0;
  border-bottom: 1px solid rgba(122,154,109,.15);
}

.gear-product:last-of-type {
  border-bottom: none;
}

.gear-product h3,
.gear-product h4 {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  font-weight: 600;
  font-size: 1rem;
  line-height: 1.4;
  margin-bottom: 6px;
  color: var(--warm-brown);
}

.gear-product h3 a,
.gear-product h4 a {
  color: var(--forest-green);
  text-decoration: underline;
  text-underline-offset: 2px;
  text-decoration-color: rgba(46,94,46,.3);
  transition: text-decoration-color 0.2s, color 0.2s;
}

.gear-product h3 a:hover,
.gear-product h4 a:hover {
  color: #9C4E30;
  text-decoration-color: rgba(156,78,48,.5);
}

.gear-product p {
  font-size: 0.92rem;
  line-height: 1.7;
  color: var(--warm-brown);
  max-width: 68ch;
}
```

---

## Order of operations

1. Change 1 (hero CSS) — test that the hero photo appears on mobile and desktop
2. Change 2a (quick-nav) — test sticky behavior and jump links
3. Change 2b (partner cards) — test two-column on desktop, stacked on mobile
4. Change 2c (section headers) — visual check only
5. Change 2d (affiliate note) — visual check only
6. Change 3 (product blocks) — find-and-replace, then check no `.belief-block` instances remain on this page
7. Deploy to Netlify and verify the quick-nav `top: 73px` clears the header correctly on the live site — adjust by a few pixels if needed

**Do not modify the banner at any step.**
