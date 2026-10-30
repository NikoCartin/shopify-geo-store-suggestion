# QA checklist

Run on desktop (about 1366 x 900) and mobile (about 390 x 844).

- [ ] Each configured country shows the correct title, store name and flags (`?geo_test=XX&geo_reset=1`).
- [ ] A visitor on their own store sees nothing.
- [ ] An unmapped country sees nothing.
- [ ] Product, collection and page links open the same item on the target store when it exists.
- [ ] Links fall back to the target home page when it does not.
- [ ] The dialog appears only after the cookie banner is answered.
- [ ] Accept: choice stored in `localStorage` for 14 days. Decline: `sessionStorage` only.
- [ ] Tab stays inside the dialog; Escape, backdrop and × close it and save "stay".
- [ ] Promotional popups listed in `PAUSE_SELECTORS` are hidden while open and restored after.
- [ ] axe-core WCAG 2.2 A/AA scan of `.geo-suggest` returns no violations.
- [ ] No requests to a third-party IP API.
