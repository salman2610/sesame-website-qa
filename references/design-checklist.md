# Design Checklist for Websites

**Domain Name:** ______  **Project ID:** ______

## 1. HTML (Structure & Semantics)

- Use valid, semantic HTML5 tags (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`) instead of `<div>` soup.
- Ensure a unique `<title>` and descriptive `<meta>` tags on every page.
- Add `alt` attributes for all meaningful images.
- Use ARIA roles/attributes only when necessary.
- Maintain proper heading hierarchy (`<h1>` → `<h6>` in logical order).
- Ensure form elements have labels and proper input types (`email`, `tel`, `date`, etc.).
- Avoid inline styles and inline event handlers (`onclick=""`).
- Validate HTML with the W3C Validator.

## 2. CSS (Styling & Accessibility)

- Use external stylesheets, not inline CSS.
- Follow responsive design principles.
- Provide sufficient color contrast.
- Use CSS variables for consistency (colors, spacing, typography).
- Ensure layout works across major browsers (cross-browser testing).
- Test with reduced motion (respect `prefers-reduced-motion`).

## 3. JavaScript (Functionality & Performance)

- Keep scripts non-blocking (`defer`/`async`).
- Use progressive enhancement (site should still work without JS).
- Validate forms on both client and server sides.
- Avoid inline JavaScript; keep scripts modular and reusable.
- Optimize DOM manipulation (batch updates, minimize reflows).
- Handle errors gracefully (use try/catch, fallback UI).
- Don't override default browser shortcuts unnecessarily.

## 4. Accessibility (WCAG / WAI-ARIA)

- Provide keyboard navigation support.
- Use focus indicators (`:focus-visible`).
- Provide ARIA labels/roles where native HTML doesn't suffice.
- Avoid content that flashes/blinks rapidly (seizure risk).
- Test with accessibility tools (e.g., Lighthouse, Axe, NVDA/JAWS).

## 5. Performance & SEO

- Optimize images (use WebP/AVIF, responsive `srcset`).
- Minify and bundle CSS/JS files.
- Implement lazy loading for images/iframes.
- Ensure fast loading times (< 4s preferred).
- Use semantic HTML for better SEO.
- Add structured data (Schema.org) where relevant.
- Ensure a mobile-friendly viewport (`<meta name="viewport">`).

## 6. Security & Compliance

- Use HTTPS and secure cookies.
- Escape/validate all user inputs (prevent XSS/CSRF).
- Don't expose sensitive info in front-end code.
- Disable autocomplete for sensitive fields (e.g., passwords).
- Use a Content Security Policy (CSP).

---

| Internal Checking done by | Verified By |
|---|---|
| Name: | Name: |
| Date: | Date: |
