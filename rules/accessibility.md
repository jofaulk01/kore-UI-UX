# Accessibility: the 10 checks

Accessible apps are easier for everyone and are legally required for many business and government clients (ADA in the US, the European Accessibility Act in the EU since June 2025). The free component libraries in [stack.md](../stack.md) handle much of this for you if you don't fight them.

> ⚠ **Risk to flag:** if you sell to larger companies, schools or governments, they may ask for WCAG 2.1/2.2 AA compliance. These checks cover most of it, but a formal audit is a separate job.

1. **Contrast:** text 4.5:1, large text and control borders 3:1. [WCAG 1.4.3, 1.4.11]
2. **Keyboard:** everything works with Tab, Shift+Tab, Enter, Space, Esc and the arrow keys. Try your app without a mouse. [WCAG 2.1.1]
3. **Visible focus:** the focused element always shows a ring. Never remove outlines without replacing them. [WCAG 2.4.7]
4. **Labels:** every input has a visible label; icon buttons have a hidden label. [WCAG 1.3.1, 4.1.2]
5. **Not color alone:** status, errors and chart series also use text, icons or patterns. [WCAG 1.4.1]
6. **Errors say how to fix it,** next to the field, and are announced to screen readers. [WCAG 3.3.1, 3.3.3]
7. **Alt text** on meaningful images; empty alt on decorative ones. [WCAG 1.1.1]
8. **Headings in order** (H1, then H2, then H3), one H1 per page. [WCAG 1.3.1]
9. **Target size** at least 24×24px. [WCAG 2.5.8]
10. **Zoom and reflow:** the app works at 200% zoom and 320px width without sideways scrolling (data tables excepted). [WCAG 1.4.4, 1.4.10]

Sources: [WCAG 2.2 quick reference](https://www.w3.org/WAI/WCAG22/quickref), [GOV.UK accessibility guidance](https://design-system.service.gov.uk/accessibility/), [Vercel Web Interface Guidelines](https://vercel.com/design/guidelines).
