# Theme integration

In `layout/theme.liquid`, near the end of `<head>` or before `</body>`:

```liquid
{%- render 'geo-store-suggest' -%}
```

In the footer section, where the localization or bottom links are rendered:

```liquid
{%- render 'footer-region-links' -%}
```

Remove any previous geolocation redirect script (for example a `fetch` to a third-party IP API followed by `window.location.href = ...`).
