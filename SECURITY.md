# Security policy

## Reporting a vulnerability

Please report security issues privately using GitHub's
**[private vulnerability reporting](../../security/advisories/new)** (Security tab → "Report a vulnerability").
Do not open a public issue for security problems.

Include what you found, steps to reproduce, and the browser you used. You should get an acknowledgement within a
few days.

## Scope and design notes

- This is a static site. There is no server-side code, database, login or user data.
- All calculations run in the visitor's browser. The only outside request is the optional town search, which sends
  the typed place name to OpenStreetMap Nominatim; no other visitor data is sent anywhere.
- The page ships a Content Security Policy that allows scripts and styles only from the site itself and network
  requests only to the site and `nominatim.openstreetmap.org`.
- Text from the catalog, target lists and search results is HTML-escaped before display.
- Browser storage (`localStorage` / `sessionStorage`) holds only display preferences and cached town-search
  results.
