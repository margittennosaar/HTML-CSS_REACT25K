# Accessibility & Performance testing before publishing

Before releasing a website or web application, it's important to check for accessibility and performance issues. These areas affect user experience, loading speed, and how well your site works for everyone — including users with disabilities and those on slow connections.

## 1. Accessibility Testing

Accessibility ensures your website is usable for people with various disabilities. This includes keyboard navigation, screen reader support, color contrast, and more.

### Tools to Use

- Lighthouse (Chrome DevTools)
  - Run via DevTools → Lighthouse tab
  - Gives scores on accessibility, performance, SEO, etc.
  - Highlights missing labels, contrast issues, keyboard traps

- axe DevTools (by Deque)
  - Browser extension (Chrome/Firefox)
  - Run quick accessibility audits with detailed explanations
  - Detects WCAG violations in real-time

- Wave (web accessibility evaluation tool)
  - Visual tool that overlays issues on your page
  - Identifies headings structure, ARIA roles, contrast issues

### Best Practices
- Use semantic HTML (`<button>`, `<nav>`, `<main>`, etc.)
- Ensure keyboard navigability (Tab, Enter, Esc)
- Add `alt` text for all meaningful images
- Label all form fields using `<label for="...">`
- Use high color contrast for readability
- Don’t rely only on color to show meaning

## 2. Performance Testing

Performance affects how fast your page loads and how smooth it feels. Users may leave if the site is too slow.

### Tools to Use

- Lighthouse (again!)
  - Identifies large JS/CSS, unused code, slow render times
  - Offers suggestions like lazy loading, caching, minification

- WebPageTest
  - Shows waterfall charts of load events
  - Highlights critical requests, time to first byte, etc.

- PageSpeed Insights
  - Google tool that shows mobile & desktop performance
  - Offers improvement suggestions + lab/field data

### Before Publishing: Optimize This

#### HTML/CSS/JS Minification
- Use tools like [Minify](https://www.minifier.org/) or your build system (e.g., Vite, Webpack)
- Remove whitespace, comments, and unnecessary code

#### Image Optimization
- Compress images
- Use modern formats like `WebP` or `AVIF`
- Add `width` and `height` attributes for layout stability

#### Efficient CSS
- Avoid deep nesting and excessive selectors
- Remove unused styles

#### JavaScript Efficiency
- Avoid blocking the main thread
- Split bundles and use lazy loading (`import()`)
- Defer or async non-critical scripts

#### Fonts
- Use system fonts when possible
- Load custom fonts asynchronously (with `font-display: swap`)
- Only load the weights you need


## Checklist

## HTML

| What to Check                    | Why It Matters                                       | How to Check                                       | Example (Code or Tip)                                                    |
| -------------------------------- | ---------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------ |
| Use semantic HTML                | Helps screen readers and improves structure          | Inspect HTML structure manually or with Lighthouse | Use `<nav>`, `<main>`, `<article>`, `<button>`                           |
| Add `lang` attribute to `<html>` | Helps screen readers detect the correct language     | Check top of HTML document                         | `<html lang="en">`                                                       |
| Add viewport meta tag            | Enables responsive behavior on mobile devices        | Inspect `<head>` section                           | `<meta name="viewport" content="width=device-width, initial-scale=1.0">` |
| Use alt text for images          | Describes content for visually impaired users        | Use Lighthouse or axe extension                    | `<img src="logo.png" alt="Company logo">`                                |
| Proper heading structure         | Improves navigation for screen readers and SEO       | Use Wave or browser accessibility tools            | Use only one `<h1>`, and nest `<h2>`, `<h3>` logically                   |
| Label all form inputs            | Ensures accessibility for users using assistive tech | Use axe or inspect labels manually                 | `<label for="email">Email</label><input id="email">`                     |
| ARIA attributes (where needed)   | Adds clarity when semantics are not enough           | Use axe DevTools to find missing/incorrect ARIA    | Add `role`, `aria-label`, `aria-hidden` where needed                     |
| Keyboard navigation              | Makes site usable without a mouse                    | Test with Tab/Shift+Tab and Enter keys manually    | Navigate forms and menus with keyboard only                              |
| Sufficient color contrast        | Improves readability, especially for low vision      | Use Lighthouse, axe, or contrast checker           | Use contrast ratio ≥ 4.5:1 for normal text                               |
| Avoid color-only indicators      | Important for users with color blindness             | Review UI manually or use Wave overlay             | Use icons, text, or patterns with color                                  |

## CSS

| What to Check                      | Why It Matters                             | How to Check                                             | Example (Code or Tip)                              |
| ---------------------------------- | ------------------------------------------ | -------------------------------------------------------- | -------------------------------------------------- |
| Responsive design (media queries)  | Ensures site looks good on all devices     | Resize browser or use Chrome DevTools device toolbar     | `@media (max-width: 768px) { ... }`                |
| Use CSS shorthand when possible    | Keeps CSS clean and efficient              | Review CSS manually                                      | Use `margin: 10px 20px;` instead of separate props |
| Avoid !important in CSS            | Makes code harder to maintain and override | Search for `!important` in code                          | Refactor styles to avoid `!important`              |
| Use `font-display: swap` for fonts | Prevents invisible text during font load   | Add `font-display: swap` in `@font-face` declaration     | `font-display: swap;` inside `@font-face`          |
| Load only required font weights    | Reduces font loading time                  | Choose specific weights when importing from Google Fonts | Use `display=swap&weights=400;700` in font URL     |

## Performance & Media

| What to Check                   | Why It Matters                               | How to Check                                            | Example (Code or Tip)                                |
| ------------------------------- | -------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------- |
| Minify HTML, CSS, JS            | Reduces file size and improves loading speed | Use build tools or online minifiers                     | Use `vite build` or `terser`                         |
| Optimize and compress images    | Saves bandwidth and speeds up load time      | Use Squoosh or TinyPNG                                  | Compress JPGs to 80% or use WebP                     |
| Use modern image formats (WebP) | Smaller and faster to load than JPEG/PNG     | Export images as WebP and test loading                  | `<img src="image.webp">`                             |
| Lazy-load images or videos      | Improves initial load speed                  | Use `loading="lazy"` attribute in `<img>` or `<iframe>` | `<img src="..." loading="lazy">`                     |
| Enable caching (server-side)    | Improves repeat visits                       | Check response headers using DevTools → Network tab     | Use `Cache-Control`, `ETag`, `Expires` headers       |
| Test on mobile + slow network   | Simulates real-world conditions              | Use Chrome DevTools throttling and device emulation     | Throttle to "Fast 3G" and test layout/responsiveness |

