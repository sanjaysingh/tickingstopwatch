# Ticking Stopwatch

Ticking Stopwatch is a full-screen stopwatch that plays a tick on each elapsed second. It is meant to be glanced at while timing something, including on a phone left awake on a desk.

**Live app:** https://tickingstopwatch.sanjaysingh.net

## What it does

- Shows elapsed time as `MM:SS`. The minutes display wraps at 99.
- Start and stop keep the elapsed time. Reset returns the display to `00:00`.
- Plays `clock-tick.mp3` once per second while running. Mute silences the tick without stopping the timer.
- Requests a screen wake lock while running so the display stays on. The lock is released on stop, reset, or when the page is hidden, and requested again when the page becomes visible.
- Measures time from a start timestamp, so the display stays aligned with wall-clock seconds.

The layout follows the system light or dark color scheme. On a small screen the digits scale to the viewport width.

## Privacy

Timing, audio, and the wake lock stay in the browser. Nothing is sent to a server.

## Run locally

Open `index.html` in a browser. Vue and Tailwind load from a CDN, and the tick sound is the local `clock-tick.mp3` file. No install or build step is required. Browsers block audio until the page has been clicked, so start the timer with the on-screen button.

## Deploy

Commits that land on `main` deploy to GitHub Pages at https://tickingstopwatch.sanjaysingh.net. Changes reach `main` through a pull request.
