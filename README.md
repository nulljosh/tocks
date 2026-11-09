<img src="icon.svg" width="80" height="80" alt="Noonday icon">

![license](https://img.shields.io/badge/license-MIT-green)

A clock that does what the iPhone clock does, in a browser tab. Formerly Horula, and Clock before that.

World clocks, alarms, a bedtime schedule, a stopwatch, timers and a nightstand mode, in twelve languages. Native on iPhone and Mac too. It loads once, works offline and installs to your home screen or dock. No account, no tracking, one small page.

**[noonday.jaybulb.com →](https://noonday.jaybulb.com)** · **[Open the app →](https://noonday.jaybulb.com/app)**

<img src="docs/screenshots/web-light.png" width="280" alt="World Clock in light mode"> <img src="docs/screenshots/web-dark.png" width="280" alt="World Clock in dark mode">

## Features

- **World clocks.** Add a city by name, see if the sun is up there, and slide time to plan across cities. Wide windows show a grid of dials.
- **Alarms.** Repeat days, label, sound and snooze. Ringing takes the whole screen and repeats until you stop it.
- **Sleep.** A bedtime, a wake time and a wind-down reminder. Hours of sleep are counted for you.
- **Stopwatch and timers.** Laps you can copy as a table, as many timers as you want, presets you pin and work and rest intervals.
- **Nightstand.** Digits, a dial or a sun dial. It dims, turns red at night and drifts a little so the screen never burns in.
- **Sweep hand.** The second hand glides every frame instead of ticking.
- **Twelve languages.** Picked from your browser or in Settings, with right to left for Arabic.
- **Backups.** One file with your alarms, cities and timers, shared with the iPhone and Mac app.

## Put a clock on your page

One iframe, no script on your side. It follows light and dark on its own.

```html
<iframe src="https://noonday.jaybulb.com/embed?city=Tokyo" width="320" height="120" style="border:0"></iframe>
<iframe src="https://noonday.jaybulb.com/embed?to=2026-12-25T00:00&label=Christmas" width="320" height="140" style="border:0"></iframe>
```

Add `&face=digital` to drop the dial, `&theme=dark` or `&theme=light` to pin a theme, `&bg=none` for a see-through background.

## Run it

```
python3 -m http.server 8000     # then open localhost:8000
./deploy.sh                      # Cloudflare Worker at noonday.jaybulb.com; a push deploys nothing
```

No build step and no dependencies. State lives in `localStorage` on the device.

## Brand

Icon, tokens and type are in `brand/BRAND.md`. The halftone art comes from `scripts/gen_art.py`. Remaining gaps against the iOS Clock are in `GAPS.md`.

MIT. See `WHITEPAPER.md` for how it works and `SECURITY.md` for reporting.
