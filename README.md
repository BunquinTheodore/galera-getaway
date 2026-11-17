# Galera Getaway

A student travel guide to Puerto Galera, Oriental Mindoro. School project for CC 100, Batangas State University.

It is a plain static site: HTML pages and one stylesheet. No build step. Open `index.html` or serve the folder with any static server.

## Pages

| File | What it is |
| --- | --- |
| `index.html` | Home with featured places, a film strip and quick facts |
| `places.html` | Places to visit, with a map |
| `activities.html` | Popular activities, tour packages and a price list |
| `hotels.html` | Stays with a budget, mid range and resort filter |
| `guide.html` | Manila to Puerto Galera route, fares, a currency converter and reminders |
| `contact.html` | Booking inquiry form and booking contacts |
| `hotlines.html` | Emergency and community hotline numbers. Linked from the footer only, not the menu |
| `credits.html` | Photo and content credits |

## Files

- `styles.css` is the only stylesheet. Its header comment explains how it is layered.
- `images/` holds every photo, including `og-image.jpg`, the picture shown in link previews. Credits are listed in `credits.html` and `credits.json`.

## How it works

- **Theme.** A glassmorphism look: a fixed ocean glow sits behind frosted translucent panels.
- **Photo cards.** On devices with a mouse, cards show the photo and title. The details rise up on hover and the photo zooms. Touch devices keep the photo on top with details underneath.
- **Hotel filter.** Built with radio inputs and sibling selectors in CSS. No script.
- **Phone menu.** On phones the menu becomes a floating glass tab bar at the bottom. It is `position: fixed` inside the header, so the header must not get `backdrop-filter`, `transform` or `filter` at phone widths.
- **Splash screen.** Markup and animation are CSS. A one line script in each page head skips it when moving between pages and keeps it for the first visit and refresh.
- **Currency converter.** An inline script in `guide.html` loads live rates from `open.er-api.com`. It falls back to rough estimates after 6 seconds or on error.

## Keeping it consistent

- The header, footer and splash markup is repeated in every page. Change all eight when you change one.
- Prices and fares are approximate and should be confirmed before booking.
- Never invent facts. Hotels without a known rate say "Rates on request".
