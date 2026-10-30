# Design decisions

| Decision | Reason |
| --- | --- |
| Suggest instead of redirect | Google advises against automatic IP redirects for multi-regional sites because they can stop users and crawlers from reaching every version ([Google Search Central](https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites)). |
| Centered dialog | Shopify moved its Geolocation app to a center popup after finding it increased checkouts in the correct currency and international conversion ([Shopify changelog](https://changelog.shopify.com/posts/improvements-to-shopify-s-geolocation-app)). |
| Country flags | Baymard found that country overlays can be mistaken for promotional popups and recommends prominent flags on mobile ([Baymard Institute](https://baymard.com/research-articles/ecommerce-homepage-ux)). |
| 14-day memory | Matches the re-prompt interval of Shopify's Geolocation app ([Shopify Help Center](https://help.shopify.com/en/manual/international/geolocation)). |
| Shopify's own country endpoint | Avoids rate-limited third-party IP APIs and sends no visitor data to another service. |
| Same-page deep link with fallback | Regional stores often use different handles; a blind same-path redirect can land on a 404. |
| Storage tied to consent | The choice is a preference, so it is persisted only when preferences processing is allowed. |
